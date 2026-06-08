# Branch Protection & Access Control Setup — Yayasan ASIB

> **Status:** ⏳ **PENDING** — Manual setup required by repo owner  
> **Last Updated:** 9 Juni 2026  
> **Setup By:** IT Coordinator (`timitasib@gmail.com`)  
> **Time Required:** ~15 minutes  
> **⚠️ IMPORTANT:** Repo is currently PUBLIC and owned by user account `amalshalih` (not org)

---

## 🚨 Current Status (Verified 9 Juni 2026)

**Repository:** `amalshalih/amalshalih`
- **Visibility:** ❌ **PUBLIC** (should be private)
- **Owner:** `amalshalih` (User account, NOT organization)
- **Branch Protection:** ❌ **NOT ENABLED**
- **Teams:** ❌ **NOT AVAILABLE** (requires organization)
- **API Access:** ❌ **NO ADMIN TOKEN** (current token has read-only access)

**What This Means:**
- Branch protection CANNOT be set up via API without admin token
- Teams CANNOT be created (requires GitHub organization)
- Repo owner (`amalshalih` user) must manually enable protection via GitHub UI
- Consider transferring repo to organization for proper access control

---

## 🔐 Why Branch Protection?

Branch protection rules prevent:
- ❌ Accidental direct pushes to `main` branch
- ❌ Force pushes that rewrite history
- ❌ Merging without code review
- ❌ Deleting important branches
- ❌ Unreviewed changes to critical files (`.openkb/`, configs)

**Goal:** Ensure all changes go through Pull Request review process.

---

## 📋 Prerequisites

Before starting, ensure:
- [ ] **CONVERT TO PRIVATE:** Change repo visibility from public to private
- [ ] **CREATE ORG (Recommended):** Transfer repo to GitHub organization for team support
- [x] You have **Admin** access to `amalshalih/amalshalih` repo (owner only)
- [ ] **Admin Token:** Generate personal access token with `repo` scope for API access
- [ ] 2FA is enforced (recommended)

### **Option A: Manual Setup via GitHub UI (Easiest)**

**Who:** Repo owner (`amalshalih` user account)  
**Time:** ~10 minutes

1. Go to: `https://github.com/amalshalih/amalshalih/settings`
2. Scroll to **"Danger Zone"**
3. Click **"Change visibility"** → Make private
4. Go to: `https://github.com/amalshalih/amalshalih/settings/branches`
5. Click **"Add branch protection rule"**
6. Follow steps in "Branch Protection Rules Setup" section below

### **Option B: Transfer to Organization (Recommended for Teams)**

**Who:** Repo owner + Org admin  
**Time:** ~20 minutes

1. Create GitHub organization: `https://github.com/organizations/new`
2. Transfer repo: Settings → Danger Zone → Transfer ownership
3. Set up teams in org: `https://github.com/orgs/YOUR-ORG/teams`
4. Enable branch protection with team restrictions

### **Option C: API Setup (Advanced)**

**Who:** IT with admin token  
**Time:** ~5 minutes (if you have admin token)

Requires personal access token with `repo` scope from repo owner.

---

## 👥 Access Levels & Teams

### **Recommended Team Structure**

| Team Name | Members | Access Level | For Who |
|-----------|---------|--------------|---------|
| `pengurus` | Ketua, Wakil, Sekretaris | **Admin** | Decision makers |
| `it-tech` | IT Coordinator, Developers | **Write** | Technical maintainers |
| `media` | Media Relations, Content Creators | **Write** | Content editors |
| `admin` | Admin staff | **Write** | Daily operations |
| `relawan` | Relawan AMMA | **Read** (or **Triage** for contributors) | Volunteers |

### **How to Create Teams**

1. Go to: `https://github.com/organizations/amalshalih/teams`
2. Click **"New team"**
3. Fill in:
   - **Team name:** e.g., `it-tech`
   - **Description:** "IT & technical maintainers"
   - **Visibility:** Visible (within org)
   - **Team notifications:** Optional email
4. Click **"Create team"**
5. Add members: Click **"Add members"** → search GitHub usernames

Repeat for each team.

---

## 🛡️ Branch Protection Rules Setup

### **Step 1: Navigate to Branch Settings**

1. Go to: `https://github.com/amalshalih/amalshalih/settings/branches`
2. Click **"Add branch protection rule"** (or edit existing `main`)
3. **Branch name pattern:** `main`

### **Step 2: Configure Protection Rules**

Enable the following settings:

#### ✅ **Require a pull request before merging**
- [x] **Require approvals** → `1` (minimum 1 reviewer)
- [ ] **Dismiss stale pull request approvals when new commits are pushed** (optional)
- [x] **Require review from Code Owners** (if CODEOWNERS file exists)

#### ✅ **Require status checks to pass before merging**
- [x] **Search for status checks** → Add:
  - `build` (if CI is set up)
  - `test` (if CI is set up)
- [x] **Require branches to be up to date before merging**

#### ✅ **Do not allow bypassing the above settings**
- [x] **Allow specific actors to bypass** → Add `pengurus` team (Admin override)

#### ✅ **Lock branch**
- [ ] **Lock branch** (optional — prevents all pushes, even via PR)

#### ✅ **Require linear history**
- [ ] **Require linear history** (prevents merge commits — enforce rebase)

#### ✅ **Allow force pushes**
- [ ] **Allow force pushes** → **DISABLED** (never allow on `main`)

#### ✅ **Allow deletions**
- [ ] **Allow deletions** → **DISABLED** (never allow deleting `main`)

### **Step 3: Save Rule**

Click **"Create"** or **"Save changes"**

---

## 📁 Protected Paths (Optional Advanced Rules)

For granular control over specific directories:

### **Rule for `.openkb/` folder**

1. Create separate rule:
   - **Branch name pattern:** `main`
   - **Restrict edits to:** `pengurus`, `it-tech` teams only
   - **Apply to:** `.openkb/**`

This ensures only authorized teams can modify knowledge base docs.

### **Rule for Config Files**

Protect critical configs:
- `wrangler.toml`
- `astro.config.mjs`
- `package.json`
- `.github/workflows/`

**Pattern:** `**/{wrangler.toml,astro.config.mjs,package.json,.github/**}`

---

## 🔑 Code Owners (Optional but Recommended)

Create `CODEOWNERS` file at repo root:

```markdown
# Code Owners for Yayasan ASIB
# Format: path @github-team

# OpenKB docs
.openkb/ @amalshalih/it-tech @amalshalih/pengurus

# Website code
src/ @amalshalih/it-tech
public/ @amalshalih/it-tech

# Config files
*.{toml,json,mjs} @amalshalih/it-tech

# GitHub workflows
.github/workflows/ @amalshalih/it-tech
```

**Effect:** Any PR touching these paths automatically requests review from specified teams.

---

## ✅ Verification Checklist

After setup, verify:

- [ ] **Try direct push to `main`** → Should be rejected
- [ ] **Create PR without approval** → Should be blocked from merging
- [ ] **Force push attempt** → Should fail
- [ ] **Team members can create branches** → Should work
- [ ] **Team members can open PRs** → Should work
- [ ] **Admin can bypass (if configured)** → Should work in emergencies

---

## 🚨 Emergency Bypass Process

In case of urgent fixes:

1. **Admin** can bypass branch protection (if allowed)
2. **Alternative:** Create PR → merge immediately with self-approval (Admin only)
3. **Document:** Add comment explaining why bypass was necessary
4. **Post-mortem:** Review if bypass was justified

---

## 📊 Access Review Schedule

**Quarterly Review** (every 3 months):

- [ ] Review team membership — remove inactive members
- [ ] Check access logs for suspicious activity
- [ ] Update CODEOWNERS if team structure changed
- [ ] Verify 2FA is still enforced
- [ ] Review branch protection rules — adjust if needed

**Next Review Date:** [Set calendar reminder for 3 months from setup date]

---

## 🆘 Troubleshooting

### **"You don't have permission to do that"**
- Check if user is in correct team
- Verify team has correct access level
- Admin should check: Settings → Manage access

### **"Branch protection rule prevents merge"**
- Ensure PR has required approvals
- Check if status checks passed (CI/CD)
- Update branch with latest `main`

### **"Can't add team member"**
- User must have joined the organization first
- Check if user has 2FA enabled (if required)
- Admin may need to resend invitation

---

## 📚 Related Resources

- **GitHub Docs:** [Branch protection rules](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-protected-branches/about-protected-branches)
- **GitHub Docs:** [Code Owners](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-code-owners)
- **GitHub Docs:** [Teams](https://docs.github.com/en/organizations/organizing-members-into-teams/about-teams)

---

## 📞 Contact & Support

| Role | Contact | For |
|------|---------|-----|
| **IT Coordinator** | timitasib@gmail.com | Technical setup, access issues |
| **Pengurus** | [Pengurus email] | Policy decisions, team approvals |

---

**Setup Completed By:** _______________  
**Setup Date:** _______________  
**Next Review:** _______________

---

*"Branch protection ensures our knowledge base and code remain secure, reviewed, and auditable. No single person should have unchecked power to modify critical files."*