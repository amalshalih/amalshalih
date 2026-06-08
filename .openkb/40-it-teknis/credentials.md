# 🔑 Credentials & Password Manager Setup

> Panduan lengkap setup, konfigurasi, dan pengelolaan credentials menggunakan Bitwarden untuk Yayasan ASIB

**Last Updated:** 7 Juni 2026  
**Status:** 🟢 Active  
**Applies to:** Tim IT, Pengurus, Semua anggota dengan akses ke sistem

---

## 📋 Daftar Isi

1. [Why Password Manager?](#why-password-manager)
2. [Bitwarden Setup](#bitwarden-setup)
3. [Organization Configuration](#organization-configuration)
4. [Credential Management](#credential-management)
5. [Secure Sharing](#secure-sharing)
6. [Emergency Access](#emergency-access)
7. [Migration Guide](#migration-guide)
8. [Best Practices](#best-practices)

---

## 🎯 Why Password Manager?

### **Problems Without Password Manager:**

❌ **Password Reuse:** Same password across multiple services  
❌ **Weak Passwords:** Easy to guess (yayasan2026, amalshalih123)  
❌ **Insecure Storage:** Passwords in WhatsApp, email, sticky notes, Excel files  
❌ **Sharing Nightmare:** Sending passwords via WhatsApp/email  
❌ **No Audit Trail:** Who has access to what?  
❌ **Offboarding Risk:** Former members still have passwords  

### **Benefits of Password Manager:**

✅ **Strong Passwords:** Generate random, complex passwords  
✅ **Unique Passwords:** Different password for every service  
✅ **Secure Storage:** Encrypted vault (AES-256 encryption)  
✅ **Secure Sharing:** Share without revealing actual password  
✅ **Access Control:** See who has access to what  
✅ **Audit Trail:** Log of all access & changes  
✅ **Emergency Access:** Trusted contacts can access in emergency  
✅ **Cross-Platform:** Works on all devices (browser, mobile, desktop)  

### **Why Bitwarden?**

| Feature | Bitwarden | LastPass | 1Password | KeePass |
|---------|-----------|----------|-----------|---------|
| **Open Source** | ✅ Yes | ❌ No | ❌ No | ✅ Yes |
| **Free Tier** | ✅ Unlimited passwords, all devices | ⚠️ Limited | ❌ No free tier | ✅ Yes (offline only) |
| **Encrypted Sharing** | ✅ Yes (free tier) | ❌ Paid only | ❌ Paid only | ⚠️ Manual |
| **Emergency Access** | ✅ Yes (free tier) | ❌ Paid only | ❌ Paid only | ❌ No |
| **Self-Hostable** | ✅ Yes | ❌ No | ❌ No | ✅ Yes |
| **Nonprofit Discount** | ✅ Yes (free for teams) | ⚠️ Limited | ✅ Yes | N/A |
| **Ease of Use** | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ | ⭐⭐⭐ |

**Decision:** Bitwarden chosen for:
- Open source (transparent security)
- Free tier sufficient for nonprofit
- Encrypted sharing included
- Emergency access feature
- Can self-host if needed later

---

## 🔧 Bitwarden Setup

### **Step 1: Create Personal Account**

**1. Visit Bitwarden:**
```
URL: https://vault.bitwarden.com
Or: https://bitwarden.com → Sign Up
```

**2. Register Account:**
```
Email: Use personal email (NOT organizational email)
       Example: nama.pribadi@gmail.com
       
Password: Create STRONG master password (20+ characters)
          Example: K7#mP9$xL2@nQ4vR8!wS1&tU5^yZ

Hint: Create a hint only YOU understand
      Example: "Favorite verse + birth year + special char"
      
Confirm Password: Re-enter same password
```

**⚠️ CRITICAL:** Master password is NEVER stored anywhere. If lost, ALL data is lost forever. Bitwarden cannot reset it.

**3. Verify Email:**
```
→ Check email inbox
→ Click verification link
→ Account activated
```

**4. Setup Two-Factor Authentication (2FA):**
```
→ Settings (gear icon) → Two-step Login
→ Enable Authenticator App
→ Scan QR code with Google Authenticator/Authy
→ Enter 6-digit code
→ Save backup codes (PRINT & STORE SECURELY)
→ Enable
```

### **Step 2: Install Bitwarden Apps**

**Browser Extension (ALL Devices):**
```
Chrome: Chrome Web Store → Search "Bitwarden" → Add to Chrome
Firefox: Firefox Add-ons → Search "Bitwarden" → Add to Firefox
Safari: Mac App Store → Search "Bitwarden" → Install
Edge: Edge Add-ons → Search "Bitwarden" → Get

After Install:
→ Click Bitwarden icon
→ Login with email & master password
→ Enable auto-fill
→ Enable auto-lock (15 minutes recommended)
```

**Mobile App (iOS/Android):**
```
iOS: App Store → Search "Bitwarden" → Get
Android: Google Play → Search "Bitwarden" → Install

After Install:
→ Open app
→ Login with email & master password
→ Enable biometric unlock (Face ID/Touch ID/Fingerprint)
→ Enable auto-lock (1 minute recommended)
```

**Desktop App (Windows/Mac/Linux):**
```
Download: https://bitwarden.com/download
→ Choose your OS
→ Download & install
→ Open app
→ Login with email & master password
```

### **Step 3: Import Existing Passwords (Optional)**

**From Browser:**

1. **Export from Browser:**
   ```
   Chrome:
   → Settings → Autofill → Password Manager
   → Three dots → Export passwords
   → Save as passwords.csv
   
   Firefox:
   → Settings → Privacy & Security → Logins and Passwords
   → Three dots → Export Logins
   → Save as logins.csv
   ```

2. **Import to Bitwarden:**
   ```
   → Bitwarden Web Vault (vault.bitwarden.com)
   → Tools → Import Data
   → Select format: "Chrome (csv)" or "Firefox (csv)"
   → Choose file
   → Click "Import Data"
   → Review imported items
   → Fix any duplicates
   ```

3. **Delete Browser Passwords:**
   ```
   ⚠️ IMPORTANT: After import, delete passwords from browser
   → Browser password manager → Delete all passwords
   → Disable browser password saving
   ```

**From Other Password Managers:**
```
→ Tools → Import Data
→ Select format (LastPass, 1Password, KeePass, etc)
→ Follow same process as above
```

### **Step 4: Setup Password Generator**

**Default Settings (Recommended):**
```
Length: 14 characters (minimum 12)
Uppercase: A-Z (include)
Lowercase: a-z (include)
Numbers: 0-9 (include)
Special Characters: !@#$%^&* (include)
Ambiguous Characters: Exclude (avoid confusion)
```

**How to Use:**
```
→ Click Bitwarden icon in browser
→ Generator tab
→ Click "Regenerate" until satisfied
→ Click "Copy"
→ Paste when creating new account/changing password
→ Bitwarden will prompt to save → Click "Yes"
```

---

## 🏢 Organization Configuration

### **Step 1: Create Organization**

**1. Create Organization:**
```
→ Bitwarden Web Vault → Settings (gear icon)
→ Organizations → Create Organization
```

**2. Select Plan:**
```
For Nonprofit:
→ Choose "Teams" plan (free for registered nonprofits)
→ Apply for nonprofit discount:
  - Upload akta yayasan
  - Upload SK Kemenkumham
  - Wait for approval (2-5 business days)

Without Nonprofit Status:
→ Choose "Free" plan (sufficient for most needs)
→ Upgrade later if needed
```

**3. Organization Details:**
```
Organization Name: Yayasan Amal Shalih Insan Bantul
Billing Email: timitasib@gmail.com (IT)
```

**4. Setup Organization:**
```
→ Organization ID assigned automatically
→ Access via: https://vault.bitwarden.com/#/organizations/[org-id]
```

### **Step 2: Create Collections**

**Collections = Folders for organizing credentials**

**Recommended Structure:**
```
Yayasan ASIB Organization
├── 📁 00-Critical-Infrastructure
│   ├── Domain (PANDI)
│   ├── Hosting (Niagahoster)
│   ├── Cloudflare DNS
│   └── SSL Certificates
├── 📁 01-Email-Accounts
│   ├── amalshalih.insanbantul@gmail.com
│   ├── timitasib@gmail.com
│   ├── media.amalshalih@gmail.com
│   └── Custom Domain Emails
├── 📁 02-Financial
│   ├── BSI Bank Account
│   ├── Payment Gateway
│   ├── Tax Accounts
│   └── Financial Reports
├── 📁 03-Social-Media
│   ├── Instagram
│   ├── Facebook
│   ├── TikTok
│   ├── YouTube
│   └── Linktree
├── 📁 04-Productivity
│   ├── Google Workspace
│   ├── Trello
│   ├── Canva
│   ├── GitHub
│   └── Sanity.io
├── 📁 05-Website
│   ├── Astro Build
│   ├── Sanity CMS
│   └── Analytics
└── 📁 99-Archive
    ├── Old Credentials
    └── Deprecated Services
```

**Create Collections:**
```
→ Organizations → [Your Org] → Collections
→ New Collection
→ Enter name (e.g., "00-Critical-Infrastructure")
→ Save
→ Repeat for all collections
```

### **Step 3: Invite Members**

**1. Invite Users:**
```
→ Organizations → [Your Org] → People
→ Invite User
→ Enter email (personal email, not organizational)
→ Select role:
  - Admin: Full control (IT only)
  - User: Can access shared collections (members)
  - Manager: Can manage collections (Koordinators)
→ Click "Save"
→ Invitation email sent
```

**2. User Accepts Invitation:**
```
→ User receives email
→ Clicks invitation link
→ Creates Bitwarden account (if doesn't have)
→ Joins organization automatically
```

**3. Assign Collection Access:**
```
→ Organizations → [Your Org] → Collections
→ Click collection name
→ Access tab
→ Check users who should have access
→ Set permissions:
  - Read-only: Can view, not edit
  - Can edit: Can modify credentials
  - Can manage: Can add/remove users
→ Save
```

**Access Matrix:**

| Collection | IT | Pengurus | Admin | Media | Relawan |
|------------|----|----------|-------|-------|---------|
| **Critical Infrastructure** | ✅ Edit | ✅ Read | ❌ | ❌ | ❌ |
| **Email Accounts** | ✅ Edit | ❌ | ✅ Edit | ❌ | ❌ |
| **Financial** | ❌ | ✅ Edit | ✅ Read | ❌ | ❌ |
| **Social Media** | ✅ Edit | ❌ | ✅ Edit | ✅ Edit | ❌ |
| **Productivity** | ✅ Edit | ✅ Read | ✅ Edit | ✅ Edit | ✅ Read |
| **Website** | ✅ Edit | ❌ | ❌ | ❌ | ✅ Read (dev only) |

### **Step 4: Setup Groups (Optional for Large Teams)**

**Groups = Bulk assign collection access**

**Recommended Groups:**
```
→ Organizations → [Your Org] → Groups
→ New Group

Group 1: "Pengurus"
- Members: All pengurus
- Collections: Critical (read), Financial (edit), All (read)

Group 2: "Tim Media"
- Members: Koordinator Media + Relawan Media
- Collections: Social Media (edit), Productivity (edit)

Group 3: "Tim IT"
- Members: IT + technical relawan
- Collections: Critical (edit), Website (edit), All (read)

Group 4: "Relawan"
- Members: All active relawan
- Collections: Productivity (read), specific project folders
```

---

## 🔐 Credential Management

### **Adding New Credentials**

**Method 1: Auto-Save (Easiest)**
```
1. Login to website as usual
2. Enter username & password
3. Bitwarden popup appears: "Save login?"
4. Click "Yes"
5. Choose collection (if in organization)
6. Credential saved
```

**Method 2: Manual Add**
```
1. Click Bitwarden icon → Add Item → Login
2. Fill details:
   - Name: Service name (e.g., "Instagram - @amalshalihinsan")
   - Username: Email/username
   - Password: Click generate for new password
   - URI: Website URL (https://instagram.com)
   - Collection: Select appropriate collection
   - Notes: Additional info (2FA status, recovery email, etc)
3. Click "Save"
```

**Method 3: Import from File**
```
1. Tools → Import Data
2. Select format
3. Upload file
4. Review & confirm
```

### **Credential Fields**

**Required Fields:**
```
Name: Clear, descriptive name
      Format: "[Service] - [Account/Role]"
      Example: "Instagram - @amalshalihinsan"
      Example: "BSI Online - Main Account"

Username: Email or username for login

Password: Generated strong password (14+ chars)
          Click generator icon → Copy → Paste

URI: Website URL (helps with auto-fill)
     Example: https://instagram.com
```

**Optional Fields:**
```
TOTP (2FA): For 2FA codes (premium feature)
            Scan QR code → Bitwarden generates codes

Notes: Additional information
       - 2FA backup codes location
       - Recovery email/phone
       - Security questions
       - Last rotation date
       - Next rotation due

Custom Fields: Add custom data
               - API keys
               - PIN codes
               - Account numbers
```

### **Credential Organization**

**Naming Convention:**
```
Format: [Service] - [Account/Role/Handle]

Examples:
✅ "Gmail - amalshalih.insanbantul@gmail.com"
✅ "Instagram - @amalshalihinsan (Public)"
✅ "BSI Banking - Main Operating Account"
✅ "Trello - timitasib@gmail.com (Admin)"
❌ "instagram password" (vague)
❌ "email" (too generic)
❌ "new account" (meaningless)
```

**Folder vs Collection:**
```
Collections: For SHARED credentials (organization)
             Access controlled by member role

Folders: For PERSONAL credentials (individual)
         Only you can access

Best Practice:
- Organizational accounts → Collections
- Personal accounts → Personal vault (not in org)
```

### **Credential Rotation**

**Schedule:**
```
Critical (Email, Domain, Hosting, Financial):
- Every 6 months (January & July)
- Immediately if suspicious activity

Important (Social Media, Productivity):
- Every 12 months (January)
- When team member leaves

Regular (Non-critical):
- When suspicious activity
- When prompted by service
```

**Rotation Process:**
```
1. Open credential in Bitwarden
2. Click password field → Generate new password
3. Copy new password
4. Login to service → Change password
5. Paste new password
6. Bitwarden prompts to update → Click "Update"
7. Verify login works with new password
8. Update notes: "Rotated [Date] by [Name]"
9. Notify authorized users (via secure channel)
```

**Rotation Log:**
```markdown
| Account | Last Rotated | Rotated By | Next Rotation | Status |
|---------|--------------|------------|---------------|--------|
| Gmail - utama | 2026-01-15 | [Name] | 2026-07-15 | ✅ OK |
| BSI Banking | 2026-01-15 | [Name] | 2026-07-15 | ✅ OK |
| Instagram | 2026-01-15 | [Name] | 2027-01-15 | ✅ OK |
```

---

## 🔗 Secure Sharing

### **Sharing Best Practices**

**DO:**
✅ Share via Bitwarden collection (encrypted)  
✅ Grant minimum necessary access (read vs edit)  
✅ Review access quarterly  
✅ Remove access immediately when no longer needed  
✅ Use emergency access for critical accounts  

**DON'T:**
❌ Share passwords via WhatsApp/email  
❌ Share via unencrypted files (Excel, Google Docs)  
❌ Write passwords on paper (except backup codes)  
❌ Share master password with anyone  
❌ Share entire organization access (use collections)  

### **Sharing Workflows**

**Scenario 1: New Member Needs Access**
```
1. IT adds user to organization
2. IT assigns user to appropriate collections
3. User receives notification
4. User can now access shared credentials
5. User sees password (can copy/auto-fill)
6. IT logs access grant in spreadsheet
```

**Scenario 2: Temporary Access for Project**
```
1. Create temporary collection: "Project-X-Temp"
2. Add credentials needed for project
3. Add user to collection with edit access
4. Set reminder for access review (end of project)
5. When project ends → Remove user from collection
6. Document in access log
```

**Scenario 3: External Partner Access**
```
1. Create specific collection for partner
2. Add only credentials they need
3. Invite external email as user
4. Set read-only access (unless edit required)
5. Set expiration date (calendar reminder)
6. Remove access when partnership ends
7. Document in access log
```

### **Access Requests**

**Process:**
```
1. User submits request via Trello card:
   "Access Request - [Name] - [Collection]"
   
2. Koordinator reviews & approves:
   - Is access necessary for role?
   - What permission level (read/edit)?
   - How long is access needed?
   
3. IT processes request:
   - Add user to collection
   - Set appropriate permissions
   - Document in access spreadsheet
   
4. User confirms access:
   - Test login to credential
   - Confirm working in Trello card
   
5. IT monitors access:
   - Quarterly review
   - Remove if no longer needed
```

**Trello Card Template:**
```
Title: Access Request - [Nama] - [Collection]

**Requested by:** [Nama]
**Role:** [Role]
**Collection:** [Collection name]
**Permission Level:** Read / Edit / Manage
**Reason:** [Why access needed]
**Duration:** Permanent / Temporary (until [date])

**Approval:**
- [ ] Koordinator approved: [Name] [Date]
- [ ] IT processed: [Name] [Date]
- [ ] Access confirmed by user: [Date]

**Notes:**
[Any additional info]
```

---

## 🚨 Emergency Access

### **What is Emergency Access?**

Emergency Access allows trusted contacts to access your Bitwarden vault in emergencies:
- You become incapacitated
- You're unavailable for extended period
- You pass away

**Types of Emergency Access:**
1. **View:** Can view all items (cannot edit)
2. **Takeover:** Can take ownership of account

### **Setup Emergency Contacts**

**Step 1: Add Emergency Contact**
```
→ Bitwarden Web Vault → Settings → Emergency Access
→ Add Emergency Contact
→ Enter email (trusted person)
→ Select type: View or Takeover
→ Wait time: 1-14 days (recommended: 7 days)
→ Click "Save"
```

**Step 2: Contact Accepts Invitation**
```
→ Contact receives email invitation
→ Clicks link
→ Creates Bitwarden account (if doesn't have)
→ Accepts emergency access
```

### **Recommended Emergency Contacts**

| Primary Account | Emergency Contact 1 | Emergency Contact 2 | Wait Time |
|-----------------|---------------------|---------------------|-----------|
| **IT (timitasib)** | Pengurus Ketua | Bendahara | 7 days |
| **Pengurus Ketua** | IT | Pengurus Sekretaris | 7 days |
| **Bendahara** | Pengurus Ketua | IT | 7 days |
| **Admin (email utama)** | IT | Koordinator Media | 3 days |

### **Emergency Access Process**

**When Emergency Contact Needs Access:**

1. **Request Access:**
   ```
   → Emergency Contact logs into their Bitwarden
   → Emergency Access tab
   → Click "Request Access" on your name
   → You receive email notification
   ```

2. **Grant Access (If You're Available):**
   ```
   → You receive email
   → Login to Bitwarden
   → Emergency Access → Approve request
   → Contact can now access your vault
   ```

3. **Emergency Access (If You're Unavailable):**
   ```
   → Contact requests access
   → You don't respond (incapacitated)
   → Wait time elapses (e.g., 7 days)
   → Contact can automatically access
   → Contact can view (or takeover) your vault
   ```

### **Emergency Access Use Cases**

**Use Case 1: IT Lead Incapacitated**
```
Scenario: IT lead hospitalized, no one can access critical accounts

Process:
1. Pengurus Ketua requests emergency access to IT vault
2. Wait 7 days (if IT doesn't respond)
3. Gain view access to all credentials
4. Access critical accounts (domain, hosting, email)
5. Manage operations until IT recovers
6. Or reassign access to new IT lead
```

**Use Case 2: Sudden Death of Key Person**
```
Scenario: Key person passes away, credentials lost

Process:
1. Emergency contact requests access
2. Wait time elapses
3. Takeover access (if granted)
4. Export all credentials
5. Distribute to appropriate people
6. Change all critical passwords
7. Re-setup 2FA with new contacts
```

**Use Case 3: Extended Unavailability**
```
Scenario: Key person traveling, no communication for weeks

Process:
1. Team requests emergency access
2. Wait time elapses (no response)
3. Gain temporary access
4. Handle urgent matters
5. Access revoked when person returns
```

### **Emergency Access Best Practices**

**DO:**
✅ Setup emergency access for ALL critical accounts  
✅ Choose at least 2 emergency contacts per account  
✅ Test emergency access process annually  
✅ Document emergency contacts in separate location  
✅ Review emergency contacts annually (people change)  

**DON'T:**
❌ Skip emergency access setup (critical risk)  
❌ Choose only 1 emergency contact (single point of failure)  
❌ Set wait time too short (<3 days)  
❌ Set wait time too long (>14 days for critical)  
❌ Forget to update when contacts leave organization  

---

## 📥 Migration Guide

### **Phase 1: Preparation (Week 1)**

**1. Audit Existing Credentials:**
```
Create spreadsheet: Credential-Audit-2026.xlsx

Columns:
- Service Name
- Current Username
- Current Password (⚠️ temporary, delete after migration)
- 2FA Enabled? (Y/N)
- 2FA Method (SMS/App/None)
- Recovery Email/Phone
- Owner/Primary User
- Collection (where it should go)
- Priority (Critical/High/Medium/Low)
```

**2. Setup Bitwarden Organization:**
```
→ Follow Section 3 (Organization Configuration)
→ Create all collections
→ Invite core team (IT, Pengurus)
→ Test sharing works
```

**3. Prepare Team:**
```
→ Announce migration plan in meeting
→ Explain why (security benefits)
→ Provide training session (30 minutes)
→ Share this documentation
→ Set deadline for completion
```

### **Phase 2: Critical Accounts (Week 2)**

**Migrate in Priority Order:**

**Day 1-2: Critical Infrastructure**
```
□ Domain (PANDI)
□ Hosting (Niagahoster)
□ Cloudflare DNS
□ SSL Certificates

Process:
1. IT logs into each service
2. Changes password to new strong password
3. Saves credential in Bitwarden (Critical Infrastructure collection)
4. Updates 2FA if needed
5. Tests login with new password
6. Documents in migration log
```

**Day 3-4: Email Accounts**
```
□ amalshalih.insanbantul@gmail.com
□ timitasib@gmail.com
□ media.amalshalih@gmail.com
□ Custom domain emails

Process:
1. Owner logs into each email account
2. Changes password
3. Saves in Bitwarden (Email Accounts collection)
4. Verifies 2FA enabled
5. Shares with appropriate team members
6. Tests login
```

**Day 5: Financial Accounts**
```
□ BSI Bank Account
□ Payment Gateway (if any)
□ Tax Accounts

Process:
1. Bendahara + IT together (dual control)
2. Change passwords
3. Save in Bitwarden (Financial collection)
4. Share with Pengurus + Bendahara
5. Test login
```

### **Phase 3: Important Accounts (Week 3)**

**Day 1-2: Social Media**
```
□ Instagram
□ Facebook
□ TikTok
□ YouTube
□ Linktree

Process:
1. Koordinator Media logs in
2. Changes password
3. Saves in Bitwarden (Social Media collection)
4. Shares with Media team
5. Tests login
```

**Day 3-4: Productivity Tools**
```
□ Google Workspace
□ Trello
□ Canva
□ GitHub
□ Sanity.io

Process:
1. Primary user logs in
2. Changes password
3. Saves in Bitwarden (Productivity collection)
4. Shares with team
5. Tests login
```

**Day 5: Website & Analytics**
```
□ Astro Build Credentials
□ Sanity CMS
□ Google Analytics (if setup)
□ Google Search Console

Process:
1. IT logs in
2. Changes password
3. Saves in Bitwarden (Website collection)
4. Shares with technical team
5. Tests login
```

### **Phase 4: Team Onboarding (Week 4)**

**Day 1-2: Core Team Training**
```
Attendees: Pengurus, Koordinators, Admin

Agenda:
1. Why password manager? (10 min)
2. Bitwarden setup demo (15 min)
3. Hands-on practice (20 min)
4. Q&A (15 min)

Hands-on:
- Each person creates personal account
- Installs browser extension
- Imports/saves 3-5 personal passwords
- Accesses shared organization credentials
- Practices generating & using passwords
```

**Day 3-4: Relawan Training**
```
Attendees: All active relawan (batch sessions)

Same agenda as core team
Focus on:
- Accessing shared credentials they need
- NOT sharing passwords outside Bitwarden
- Reporting suspicious activity
```

**Day 5: Migration Complete**
```
Checklist:
□ All credentials migrated
□ All team members trained
□ All extensions installed
□ Old password storage deleted
□ Emergency access setup
□ Access review completed
□ Migration documented
```

### **Phase 5: Cleanup (Week 5)**

**1. Delete Old Password Storage:**
```
□ Delete Excel/Google Sheets with passwords
□ Empty trash/recycle bin
□ Delete WhatsApp messages with passwords
□ Delete email threads with passwords
□ Shred any printed password lists
```

**2. Disable Browser Password Saving:**
```
Chrome:
→ Settings → Autofill → Password Manager
→ Turn off "Offer to save passwords"
→ Delete all saved passwords

Firefox:
→ Settings → Privacy & Security → Logins and Passwords
→ Uncheck "Ask to save logins"
→ Remove all saved logins

Safari:
→ Preferences → AutoFill → Edit
→ Remove all passwords
```

**3. Final Verification:**
```
□ Login test for all critical accounts
□ Verify all team members can access what they need
□ Confirm 2FA enabled on all critical accounts
□ Review emergency access setup
□ Document lessons learned
```

---

## ✅ Best Practices

### **Daily Habits:**

**Every Day:**
```
✅ Use Bitwarden for ALL logins (no exceptions)
✅ Let Bitwarden generate passwords for new accounts
✅ Lock Bitwarden when stepping away (Win+Shift+L / Cmd+Shift+L)
✅ Verify auto-fill is correct before submitting
```

**Every Week:**
```
✅ Review vault for duplicates
✅ Check for weak/old passwords
✅ Verify 2FA enabled on critical accounts
✅ Review access logs (organization admin)
```

**Every Month:**
```
✅ Rotate 1-2 critical passwords (staggered schedule)
✅ Review emergency contacts
✅ Audit collection access (who has access to what)
✅ Export encrypted backup (store securely)
```

**Every Quarter:**
```
✅ Full access review (remove inactive users)
✅ Test emergency access process
✅ Review & update collections structure
✅ Security audit (check for breaches)
```

### **Security Rules:**

**ALWAYS:**
✅ Use generated passwords (14+ characters)  
✅ Enable 2FA on every account that supports it  
✅ Keep master password secret (never share)  
✅ Lock Bitwarden when not in use  
✅ Review access logs regularly  
✅ Update credentials immediately when someone leaves  

**NEVER:**
❌ Share master password with anyone  
❌ Share credentials outside Bitwarden  
❌ Store passwords in plain text  
❌ Use same password twice  
❌ Click "Remember Password" in browsers  
❌ Access Bitwarden on public/shared computers  
❌ Skip 2FA setup  

### **Common Mistakes:**

**Mistake 1: Weak Master Password**
```
❌ "yayasan2026"
❌ "amalshalih123"
❌ "password123"

✅ "K7#mP9$xL2@nQ4vR8!wS1&tU5^yZ"
✅ Use passphrase: "BlueTiger$Runs7Fast@Night"
```

**Mistake 2: Sharing Master Password**
```
Scenario: "Trust me, I'm pengurus"

Response: "Bitwarden is designed so NO ONE needs your master password.
           I'll share credentials via organization collections instead."
```

**Mistake 3: Not Using Collections**
```
❌ All credentials in personal vault, shared via WhatsApp

✅ All organizational credentials in organization collections,
   access controlled by role
```

**Mistake 4: Skipping 2FA**
```
❌ "Password is enough"

✅ Password + 2FA = Real security
   Password alone = False sense of security
```

**Mistake 5: Not Reviewing Access**
```
❌ "We trust everyone"

✅ Trust but verify:
   - Quarterly access reviews
   - Immediate revocation when leaving
   - Audit logs show who accessed what
```

---

## 📞 Support & Resources

| Resource | Link/Contact |
|----------|--------------|
| **Bitwarden Support** | https://bitwarden.com/help |
| **IT Lead** | timitasib@gmail.com |
| **Bitwarden Download** | https://bitwarden.com/download |
| **Nonprofit Discount** | https://bitwarden.com/nonprofit/ |
| **Self-Hosting Guide** | https://bitwarden.com/help/install-on-premises/ |
| **Emergency Access Guide** | https://bitwarden.com/help/emergency-access/ |

---

**Dokumen ini internal & sensitif — jangan share ke pihak luar**  
**Last reviewed:** 7 Juni 2026  
**Next review:** 7 Desember 2026  
**Access Level:** IT (full), Pengurus (full), Members (relevant sections)

**Required Acknowledgment:**
```
Saya telah membaca, memahami, dan berkomitmen untuk menggunakan Bitwarden 
sesuai panduan ini untuk semua credentials Yayasan ASIB.

Nama: _________________
Role: _________________
Tanggal: _________________
Tanda Tangan: _________________
```