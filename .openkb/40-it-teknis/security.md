# 🔒 Security Guidelines & Procedures

> Panduan lengkap keamanan digital, 2FA setup, phishing prevention, dan incident response untuk Yayasan ASIB

**Last Updated:** 7 Juni 2026  
**Status:** 🟢 Active  
**Applies to:** Semua anggota, relawan, dan pihak dengan akses ke sistem Yayasan ASIB

---

## 📋 Daftar Isi

1. [Security Principles](#security-principles)
2. [Password Security](#password-security)
3. [Two-Factor Authentication (2FA)](#two-factor-authentication-2fa)
4. [Device Security](#device-security)
5. [Phishing Prevention](#phishing-prevention)
6. [Data Protection](#data-protection)
7. [Access Control](#access-control)
8. [Incident Response](#incident-response)
9. [Security Checklist](#security-checklist)

---

## 🎯 Security Principles

### **5 Prinsip Keamanan Digital ASIB:**

1. **Defense in Depth** — Multiple layers of security (password + 2FA + monitoring)
2. **Least Privilege** — Give minimum access necessary for role
3. **Zero Trust** — Verify explicitly, never trust implicitly
4. **Security by Default** — Secure settings as default, not optional
5. **Continuous Vigilance** — Security is ongoing, not one-time setup

### **Security Mindset:**

> "Keamanan bukan tentang teknologi, tapi tentang kebiasaan. Satu klik salah bisa kompromikan semua sistem."

### **Shared Responsibility:**

| Role | Security Responsibilities |
|------|---------------------------|
| **IT** | Setup security controls, monitor threats, respond to incidents, train members |
| **Pengurus** | Approve access requests, oversee security policy, handle escalations |
| **Koordinator** | Ensure team follows security practices, report suspicious activity |
| **All Members** | Use strong passwords, enable 2FA, report phishing, lock devices |

---

## 🔐 Password Security

### **Password Requirements:**

**Minimum Standards:**
- ✅ Minimum **12 characters** (longer is better)
- ✅ Mix of **uppercase** (A-Z) and **lowercase** (a-z)
- ✅ At least **1 number** (0-9)
- ✅ At least **1 symbol** (!@#$%^&* etc)
- ✅ **No dictionary words** (avoid "password", "yayasan", "amalshalih")
- ✅ **Unique per service** (never reuse passwords)

**Password Strength Examples:**

```
❌ Weak: password123
❌ Weak: amalshalih2026
❌ Weak: yayasanASIB!
⚠️  Medium: AmalShalih2026!
✅  Strong: K7#mP9$xL2@nQ4
✅  Strong: BlueTiger$Runs7Fast@Night
✅  Strong: 3lePh@nt&Fly1ng#2026
```

### **Password Manager (MANDATORY):**

**Recommended:** **Bitwarden** (free, open-source, cross-platform)

**Why Password Manager?**
- Generate strong, random passwords
- Store securely in encrypted vault
- Auto-fill on websites/apps
- Share credentials securely with team
- Audit password health

**Setup Bitwarden:**

1. **Install:**
   - Browser extension: Chrome, Firefox, Safari, Edge
   - Mobile app: iOS, Android
   - Desktop app: Windows, Mac, Linux

2. **Create Account:**
   - Email: Use personal email (not organizational)
   - Master Password: Make it VERY strong (20+ characters)
   - Enable 2FA for Bitwarden account

3. **Create Organization:**
   - Name: "Yayasan ASIB"
   - Invite members via email
   - Create collections: Email, Hosting, Social Media, Financial, etc

4. **Import/Add Credentials:**
   - Manually add each credential
   - Or import from browser (Settings → Import Data)
   - Categorize into collections

**Alternative Password Managers:**
- 1Password (paid, user-friendly)
- KeePass (free, offline, advanced)
- LastPass (free tier limited)

**⚠️ NEVER:**
- Store passwords in plain text files
- Share passwords via WhatsApp/email
- Write passwords on sticky notes
- Use browser's "Save Password" without master password
- Reuse passwords across services

### **Password Rotation:**

**Schedule:**

| Account Type | Rotation Frequency | Next Rotation |
|--------------|-------------------|---------------|
| **Critical** (Email, Domain, Hosting, Financial) | Every 6 months | January & July |
| **Important** (Social Media, Trello, Canva) | Every 12 months | January |
| **Regular** (Non-critical services) | When suspicious activity | As needed |
| **Compromised** | Immediately | ASAP |

**Rotation Process:**

1. **Generate New Password:**
   - Use Bitwarden password generator
   - Length: 16+ characters
   - Include all character types

2. **Update at Service:**
   - Login to service
   - Go to Security/Account Settings
   - Change password
   - Save new password

3. **Update Password Manager:**
   - Bitwarden will prompt to update
   - Confirm update
   - Verify auto-fill works

4. **Notify Authorized Users:**
   - Share via Bitwarden (secure share)
   - Don't send via WhatsApp/email
   - Confirm they received & updated

5. **Test Login:**
   - Logout
   - Login with new password
   - Verify 2FA still works

6. **Document:**
   - Update spreadsheet: `IT/Security/Password-Rotation-2026.xlsx`
   - Note: Account, Date Rotated, Next Rotation, PIC

### **Emergency Password Reset:**

**If Locked Out:**

1. **Use Recovery Email:**
   - Most services allow reset via recovery email
   - Recovery for all accounts: timitasib@gmail.com

2. **Contact IT:**
   - IT can reset accounts with admin access
   - Verify identity before reset

3. **Emergency Access (Bitwarden):**
   - Setup emergency contact in Bitwarden
   - Contact can request access after timeout period
   - Use for critical accounts only

---

## 📱 Two-Factor Authentication (2FA)

### **What is 2FA?**

Two-Factor Authentication adds a second layer of security:
1. **Something you know** — Password
2. **Something you have** — Phone with authenticator app

Even if password is stolen, attacker can't login without 2FA code.

### **2FA Methods:**

| Method | Security | Convenience | Recommendation |
|--------|----------|-------------|----------------|
| **Authenticator App** (Google Auth, Authy) | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐ | ✅ **RECOMMENDED** |
| **SMS Code** | ⭐⭐⭐ | ⭐⭐⭐⭐ | ⚠️ Acceptable (not ideal) |
| **Email Code** | ⭐⭐ | ⭐⭐⭐ | ⚠️ Backup only |
| **Hardware Key** (YubiKey) | ⭐⭐⭐⭐⭐ | ⭐⭐ | ✅ Best for critical accounts |
| **Backup Codes** | ⭐⭐⭐⭐ | ⭐ | ✅ Emergency backup |

### **Mandatory 2FA Accounts:**

**Critical (2FA REQUIRED):**
- ✅ All email accounts (Gmail, custom domain)
- ✅ Domain registrar (PANDI)
- ✅ Hosting (cPanel, Niagahoster)
- ✅ Google Workspace
- ✅ Password manager (Bitwarden)
- ✅ Financial accounts (bank, payment gateway)

**Important (2FA STRONGLY RECOMMENDED):**
- ✅ Social media (Instagram, Facebook, TikTok, YouTube)
- ✅ Trello (admin accounts)
- ✅ GitHub
- ✅ Canva (team admin)
- ✅ Cloudflare

### **2FA Setup Guide (Google Authenticator):**

**Step 1: Install App**
- Download: Google Authenticator (iOS/Android)
- Alternative: Authy (multi-device sync)

**Step 2: Enable 2FA on Service**
```
Example: Gmail
1. Login to Gmail
2. Settings → Accounts and Import → Security
3. 2-Step Verification → Get Started
4. Enter password
5. Choose "Authenticator App"
6. Scan QR code with Google Auth
7. Enter 6-digit code from app
8. Save backup codes (PRINT THEM!)
9. Confirm & enable
```

**Step 3: Save Backup Codes**
- Download/print backup codes
- Store in 3 locations:
  1. IT (timitasib@gmail.com holder)
  2. Pengurus Ketua
  3. Bendahara
- Keep in secure location (safe, locked drawer)

**Step 4: Test 2FA**
- Logout from service
- Login with password
- Enter 6-digit code from app
- Verify login successful

### **2FA Best Practices:**

**DO:**
- ✅ Use authenticator app (not SMS)
- ✅ Save backup codes in multiple locations
- ✅ Test 2FA after setup
- ✅ Keep phone secure (PIN/biometric lock)
- ✅ Backup phone (cloud backup for authenticator)

**DON'T:**
- ❌ Share 2FA codes with anyone
- ❌ Screenshot 2FA codes (delete after setup)
- ❌ Lose phone without backup codes
- ❌ Disable 2FA for convenience

### **2FA Recovery (Lost Phone):**

**Scenario 1: Have Backup Codes**
1. Use backup code to login
2. Disable old 2FA
3. Setup new 2FA on new phone
4. Save new backup codes

**Scenario 2: No Backup Codes**
1. Contact IT (for organizational accounts)
2. Verify identity (phone call, security questions)
3. IT resets 2FA from admin panel
4. Setup new 2FA on new phone
5. Save new backup codes immediately

**Scenario 3: Personal Account**
1. Use account recovery process
2. Verify identity via email/phone
3. Reset 2FA
4. Setup new 2FA
5. Save backup codes

### **2FA Setup Checklist:**

```
[ ] Email Accounts
    [ ] amalshalih.insanbantul@gmail.com
    [ ] timitasib@gmail.com
    [ ] media.amalshalih@gmail.com
    [ ] admin@amalshalih.or.id (if direct access)
    
[ ] Infrastructure
    [ ] PANDI (domain)
    [ ] Cloudflare (DNS)
    [ ] Niagahoster (hosting)
    [ ] Google Workspace
    
[ ] Services
    [ ] Bitwarden (password manager)
    [ ] Trello
    [ ] GitHub
    [ ] Canva
    [ ] Meta Business Suite (IG/FB)
    [ ] TikTok
    [ ] YouTube
    
[ ] Financial
    [ ] BSI Online Banking
    [ ] Payment Gateway (if any)
```

---

## 💻 Device Security

### **Device Requirements:**

**All devices accessing ASIB systems must have:**

1. **Screen Lock:**
   - PIN/Password: Minimum 6 digits
   - Biometric: Fingerprint/Face ID (recommended)
   - Auto-lock: 5 minutes maximum

2. **Encryption:**
   - **Windows:** BitLocker (Pro) or Device Encryption (Home)
   - **Mac:** FileVault (System Preferences → Security)
   - **iPhone:** Enabled by default with passcode
   - **Android:** Settings → Security → Encrypt Phone

3. **Antivirus:**
   - **Windows:** Windows Defender (built-in) + Malwarebytes (free)
   - **Mac:** Built-in protection + Malwarebytes (free)
   - **Mobile:** Built-in protection (keep OS updated)

4. **OS Updates:**
   - Enable automatic updates
   - Install within 7 days of release
   - Don't skip major updates

### **Device Security Checklist:**

**Windows:**
```
[ ] Windows Hello (PIN/Biometric) enabled
[ ] BitLocker encryption enabled
[ ] Windows Defender active
[ ] Automatic updates enabled
[ ] Firewall enabled
[ ] Guest account disabled
[ ] Admin account password protected
```

**Mac:**
```
[ ] FileVault encryption enabled
[ ] Touch ID / Password enabled
[ ] Automatic updates enabled
[ ] Firewall enabled (System Preferences → Security)
[ ] Find My Mac enabled
[ ] Gatekeeper set to "App Store and identified developers"
```

**iPhone/iPad:**
```
[ ] Face ID / Touch ID enabled
[ ] Auto-lock: 5 minutes or less
[ ] Find My iPhone enabled
[ ] iOS updated to latest version
[ ] Erase Data enabled (after 10 failed attempts)
[ ] USB Restricted Mode enabled
```

**Android:**
```
[ ] Fingerprint / PIN enabled
[ ] Device encryption enabled
[ ] Find My Device enabled
[ ] Android updated to latest version
[ ] Google Play Protect enabled
[ ] Unknown sources disabled
```

### **Prohibited Activities:**

**NEVER on ASIB devices:**
- ❌ Install unapproved software
- ❌ Disable security features
- ❌ Share device with unauthorized person
- ❌ Leave device unattended ( unlocked)
- ❌ Connect to public Wi-Fi without VPN
- ❌ Click suspicious links/attachments
- ❌ Store personal sensitive data (KTP, KK, etc)

### **Lost/Stolen Device:**

**Immediate Actions:**

1. **Remote Lock/Wipe:**
   - **iPhone:** iCloud.com → Find My iPhone → Lost Mode
   - **Android:** google.com/android/find → Lock/Erase
   - **Windows:** account.microsoft.com/devices → Find My Device
   - **Mac:** iCloud.com → Find My Mac → Lock/Erase

2. **Change Passwords:**
   - Change password for all accounts accessed from device
   - Prioritize: Email, financial, social media

3. **Notify IT:**
   - Report to IT immediately
   - Provide: Device type, last known location, accounts accessed

4. **Monitor Accounts:**
   - Check login activity on critical accounts
   - Look for suspicious activity
   - Report any unauthorized access

5. **File Police Report (if sensitive data):**
   - For stolen device with sensitive data
   - Required for insurance claim
   - Document for legal protection

---

## 🎣 Phishing Prevention

### **What is Phishing?**

Phishing is when attackers pretend to be legitimate organizations to steal:
- Passwords
- Credit card numbers
- Personal information
- Money

**Common Phishing Types:**
- **Email Phishing:** Fake emails asking for credentials
- **SMS Phishing (Smishing):** Fake text messages
- **Voice Phishing (Vishing):** Fake phone calls
- **Social Media Phishing:** Fake profiles/messages

### **Phishing Red Flags:**

**🚨 Urgency & Threats:**
```
❌ "Your account will be suspended in 24 hours!"
❌ "Immediate action required!"
❌ "Verify your account now or lose access!"

✅ Legitimate organizations NEVER pressure you to act immediately.
```

**🚨 Suspicious Sender:**
```
❌ Email from: "support@gmai1.com" (note the "1" instead of "l")
❌ Email from: "Yayasan ASIB <personal@gmail.com>"
❌ Display name says "Bank BSI" but email is "bsi-support@yahoo.com"

✅ Always check the actual email address, not just display name.
```

**🚨 Generic Greetings:**
```
❌ "Dear Customer"
❌ "Dear User"
❌ "Dear Member"

✅ Legitimate organizations usually use your name.
```

**🚨 Suspicious Links:**
```
❌ Hover over link shows: "http://amalshalih-verify.ru/login"
❌ Shortened URLs: bit.ly/xyz123 (could go anywhere)
❌ Misspelled domains: "arnalshalih.or.id" instead of "amalshalih.or.id"

✅ Hover over links before clicking. Check the actual URL.
```

**🚨 Requests for Sensitive Information:**
```
❌ "Please verify your password"
❌ "Send your KTP photo for verification"
❌ "Confirm your bank account details"

✅ Legitimate organizations NEVER ask for passwords via email.
```

**🚨 Poor Grammar/Spelling:**
```
❌ "Dear valued customer, we has detected suspicious activity..."
❌ "Click here to verifi your account"

✅ Professional organizations proofread their communications.
```

**🚨 Unexpected Attachments:**
```
❌ Invoice attached (you didn't order anything)
❌ "Receipt.pdf.exe" (executable disguised as PDF)
❌ "Document.zip" from unknown sender

✅ Don't open attachments from unknown senders.
```

### **Phishing Examples:**

**Example 1: Fake Email Login Request**
```
From: "Google Security <security@google-verify.com>"
Subject: "Suspicious Activity Detected"

Dear User,

We detected unusual activity on your account. Please verify 
your identity immediately or your account will be suspended.

Click here to verify: http://google-security.ru/verify

Thank you,
Google Security Team
```

**Red Flags:**
- ❌ Sender domain is "google-verify.com" (not google.com)
- ❌ Generic greeting "Dear User"
- ❌ Urgency threat ("suspended")
- ❌ Suspicious link (google-security.ru)
- ❌ No signature with contact info

**What to Do:**
- ❌ DON'T click the link
- ❌ DON'T reply
- ✅ DO forward to IT: timitasib@gmail.com
- ✅ DO delete the email

**Example 2: Fake Donation Request**
```
From: "Yayasan ASIB <amalshalih.personal@gmail.com>"
Subject: "Urgent Donation Request"

Assalamu'alaikum,

We need urgent donations for disaster relief. Please transfer 
to account: 1234567890 (BCA) a.n Personal Name

May Allah bless you.

Yayasan ASIB
```

**Red Flags:**
- ❌ Personal Gmail instead of official domain
- ❌ Personal bank account (not yayasan)
- ❌ No official letterhead
- ❌ No contact information
- ❌ Vague disaster (no details)

**What to Do:**
- ❌ DON'T transfer money
- ❌ DON'T forward to others
- ✅ DO verify via official channel (call kantor)
- ✅ DO report to IT

### **Phishing Prevention Best Practices:**

**BEFORE Clicking:**
1. **Check Sender:** Verify email address (not just display name)
2. **Hover Over Links:** See actual URL before clicking
3. **Look for Red Flags:** Urgency, threats, generic greetings
4. **Verify via Different Channel:** Call sender to confirm
5. **When in Doubt:** Don't click, report to IT

**Email Security Settings:**
```
Gmail Settings:
1. Settings → See all settings
2. General → Enable "Warn me about suspicious links"
3. Filters → Create filter for suspicious domains
4. Enable 2FA (mandatory)
```

**Browser Protection:**
```
Chrome:
1. Settings → Privacy and Security
2. Enable "Safe Browsing" (Standard or Enhanced)
3. Enable "Always use secure connections"

Firefox:
1. Settings → Privacy & Security
2. Enable "Enhanced Tracking Protection"
3. Enable "Block dangerous content"
```

### **If You Clicked Phishing Link:**

**Immediate Actions:**

1. **Disconnect from Internet:**
   - Turn off Wi-Fi
   - Unplug Ethernet cable
   - Prevents malware from communicating

2. **Change Passwords:**
   - From different, clean device
   - Start with email, financial, social media
   - Enable/re-enable 2FA

3. **Scan for Malware:**
   - Run full antivirus scan
   - Use Malwarebytes (free) for second opinion
   - Quarantine/remove any threats found

4. **Monitor Accounts:**
   - Check login activity
   - Look for unauthorized transactions
   - Enable login notifications

5. **Report to IT:**
   - Forward phishing email
   - Provide details: What clicked, when, what happened
   - IT can block domain/email for organization

6. **Consider Factory Reset (if severe):**
   - Backup important files (scan first)
   - Factory reset device
   - Restore from clean backup

---

## 📂 Data Protection

### **Data Classification:**

| Classification | Examples | Access | Storage | Sharing |
|----------------|----------|--------|---------|---------|
| **Public** | Website content, social media posts | Everyone | Public folders | No restrictions |
| **Internal** | SOPs, meeting notes, internal docs | All members | Shared folders | Internal only |
| **Confidential** | Donatur data, financial records, credentials | Authorized only | Restricted folders | Need-to-know |
| **Highly Confidential** | Passwords, 2FA codes, backup codes, KTP data | IT + Pengurus only | Encrypted storage | Never share |

### **Data Handling Guidelines:**

**Confidential Data (Donatur, Financial):**
- ✅ Store in password-protected files
- ✅ Encrypt before sharing
- ✅ Share via secure channels (Bitwarden, encrypted email)
- ✅ Delete when no longer needed
- ❌ Never share via WhatsApp
- ❌ Never store on personal devices without encryption

**Credentials (Passwords, API Keys):**
- ✅ Store in Bitwarden (password manager)
- ✅ Share via Bitwarden secure sharing
- ✅ Rotate regularly
- ❌ Never share via email/WhatsApp
- ❌ Never commit to Git

**Personal Data (KTP, KK, Phone Numbers):**
- ✅ Store in restricted folder
- ✅ Access limited to authorized personnel
- ✅ Redact sensitive info when possible
- ❌ Never share publicly
- ❌ Delete when no longer needed

### **Secure File Sharing:**

**Internal Sharing:**
1. **Google Drive:**
   - Share with specific people (not "anyone with link")
   - Set appropriate permissions (Viewer, Commenter, Editor)
   - Use shared drives for organizational files

2. **Email (Encrypted):**
   - Use ProtonMail for sensitive emails (free tier)
   - Or use Gmail with confidential mode
   - Password-protect attachments
   - Send password via different channel (WA/phone)

**External Sharing:**
1. **Public Files:**
   - Use "Anyone with link can view"
   - Set expiration date if possible
   - Monitor access logs

2. **Confidential Files:**
   - Don't share externally unless necessary
   - If must share: password-protect + encrypt
   - Use NDA (Non-Disclosure Agreement)
   - Track who has access

### **Data Retention:**

| Data Type | Retention Period | Disposal Method |
|-----------|------------------|-----------------|
| **Financial Records** | 7 years | Secure delete + shred physical copies |
| **Donatur Data** | Active + 3 years | Anonymize or secure delete |
| **Employee/Relawan Records** | Active + 3 years | Secure delete |
| **Meeting Minutes** | Permanent (archive) | N/A |
| **Credentials (old)** | After rotation | Secure delete from all locations |
| **Backup Codes (used)** | After use | Shred physical copies |

### **Data Breach Response:**

**If Data is Compromised:**

1. **Contain:**
   - Revoke compromised access immediately
   - Change passwords
   - Disconnect affected systems

2. **Assess:**
   - What data was exposed?
   - How many people affected?
   - How did breach occur?

3. **Notify:**
   - Notify affected individuals
   - Report to Pengurus
   - Consider legal requirements (UU PDP)

4. **Remediate:**
   - Fix vulnerability that caused breach
   - Implement additional controls
   - Monitor for further suspicious activity

5. **Document:**
   - Record all details of breach
   - Lessons learned
   - Update security policy

---

## 🔑 Access Control

### **Access Control Principles:**

1. **Need-to-Know:** Only access necessary for role
2. **Least Privilege:** Minimum permissions required
3. **Separation of Duties:** Critical tasks require multiple people
4. **Audit Trail:** All access is logged and monitored

### **Access Request Process:**

```
1. REQUEST
   - User submits Trello card: "Access Request - [Name] - [Resource]"
   - Specify: Resource, permission level, reason, duration
   
2. APPROVE
   - Koordinator reviews & approves
   - IT verifies against access matrix
   
3. SETUP
   - IT grants access
   - Configure 2FA if required
   - Document in spreadsheet
   
4. VERIFY
   - User tests access
   - Confirm working in Trello card
   
5. MONITOR
   - IT monitors access logs
   - Quarterly access review
```

### **Access Matrix:**

| Resource | IT | Pengurus | Admin | Media | Relawan |
|----------|----|----------|-------|-------|---------|
| **Domain (PANDI)** | ✅ Full | ✅ View | ❌ | ❌ | ❌ |
| **Hosting (cPanel)** | ✅ Full | ✅ View | ❌ | ❌ | ❌ |
| **Email (Primary)** | ✅ Full | ❌ | ✅ Limited | ❌ | ❌ |
| **Google Drive (Shared)** | ✅ Full | ✅ Full | ✅ Limited | ✅ Limited | ✅ Folder |
| **Trello (Admin)** | ✅ Full | ✅ Full | ❌ | ✅ Board | ✅ Member |
| **Social Media Login** | ✅ Recovery | ❌ | ✅ Full | ✅ Full | ❌ |
| **Financial Data** | ❌ | ✅ Full | ✅ Limited | ❌ | ❌ |
| **Credentials (Bitwarden)** | ✅ Full | ✅ Critical | ❌ | ❌ | ❌ |

### **Access Review (Quarterly):**

**Timeline:** Every 3 months (Jan, Apr, Jul, Oct)

**Process:**
1. IT exports access list for all systems
2. Review per user: Still need this access?
3. Update status: Active, Inactive, Needs Adjustment
4. Revoke unnecessary access
5. Document review results

**Checklist:**
```
[ ] Review Google Drive sharing
[ ] Review Trello board members
[ ] Review Bitwarden organization members
[ ] Review social media access
[ ] Review GitHub repository access
[ ] Update access spreadsheet
[ ] Revoke inactive user access
[ ] Report to Pengurus
```

### **Offboarding Access Revocation:**

**When user leaves (resigns, inactive, terminated):**

**Immediate (within 24 hours):**
- [ ] Remove from Google Drive
- [ ] Remove from Trello boards
- [ ] Remove from Bitwarden organization
- [ ] Remove from Canva team
- [ ] Remove from GitHub organization
- [ ] Remove from social media (if had access)
- [ ] Change shared passwords they knew
- [ ] Revoke 2FA backup codes they had
- [ ] Update access spreadsheet

**Verification:**
- [ ] IT confirms all access revoked
- [ ] Koordinator verifies no remaining access
- [ ] Document in offboarding checklist

---

## 🚨 Incident Response

### **Security Incident Types:**

| Type | Severity | Response Time | Examples |
|------|----------|---------------|----------|
| **Critical** | Immediate (1 hour) | Account compromised, data breach, ransomware |
| **High** | 4 hours | Phishing successful, lost device with sensitive data |
| **Medium** | 24 hours | Suspicious activity, failed attack attempt |
| **Low** | 72 hours | Policy violation, minor security gap |

### **Incident Response Process:**

**Phase 1: Detection & Reporting**
```
1. Identify incident (user, monitoring, external report)
2. Report to IT immediately (timitasib@gmail.com)
3. IT assesses severity
4. Notify Pengurus (for Critical/High)
5. Document initial details
```

**Phase 2: Containment**
```
1. Isolate affected systems
2. Revoke compromised access
3. Change passwords
4. Disconnect from network (if malware)
5. Preserve evidence (screenshots, logs)
```

**Phase 3: Eradication**
```
1. Remove malware/threat
2. Patch vulnerability
3. Clean affected systems
4. Verify threat eliminated
```

**Phase 4: Recovery**
```
1. Restore from clean backup
2. Re-enable systems
3. Monitor for re-infection
4. Verify normal operation
```

**Phase 5: Lessons Learned**
```
1. Document incident timeline
2. Identify root cause
3. Recommend improvements
4. Update security policy
5. Train users (if human error)
```

### **Specific Incident Playbooks:**

**Playbook 1: Account Compromised**
```
1. Change password immediately
2. Revoke all active sessions
3. Check recent activity (login history)
4. Enable/re-setup 2FA
5. Notify contacts (if spam sent from account)
6. Monitor for identity theft
7. Document incident
```

**Playbook 2: Phishing Successful**
```
1. Disconnect device from internet
2. Change passwords (from clean device)
3. Run full antivirus scan
4. Check financial accounts for fraud
5. Enable fraud alerts
6. Monitor credit report
7. Report to IT & Pengurus
8. Consider police report (if financial loss)
```

**Playbook 3: Lost/Stolen Device**
```
1. Remote lock/wipe (Find My iPhone/Android)
2. Change passwords for all accounts on device
3. Notify IT
4. File police report (if sensitive data)
5. Monitor accounts for suspicious activity
6. Replace device
7. Restore from backup
```

**Playbook 4: Ransomware Attack**
```
1. Disconnect from network immediately
2. Don't pay ransom (no guarantee of recovery)
3. Identify ransomware variant (ID Ransomware website)
4. Check if decryptor available (No More Ransom project)
5. Restore from clean backup
6. Rebuild affected systems
7. Report to police (if critical)
8. Review backup strategy
```

### **Incident Contact List:**

| Role | Contact | Availability |
|------|---------|--------------|
| **IT Lead** | timitasib@gmail.com | 24/7 (emergency) |
| **Pengurus Ketua** | [Kontak] | Business hours |
| **Hosting Support** | [Phone/Chat] | 24/7 |
| **Domain Registrar** | [Email/Phone] | Business hours |
| **Local Police (Cyber Crime)** | [Phone] | 24/7 |

### **Incident Reporting Template:**

```markdown
# Security Incident Report

## Basic Information
- **Date/Time:** [DD MMM YYYY HH:MM]
- **Reported by:** [Name]
- **Severity:** Critical/High/Medium/Low
- **Status:** Open/Contained/Resolved

## Incident Details
- **Type:** [Account Compromise/Phishing/Data Breach/Malware/etc]
- **Affected Systems:** [List systems/accounts]
- **Description:** [What happened]

## Timeline
- [HH:MM] Incident occurred
- [HH:MM] Detected
- [HH:MM] Reported to IT
- [HH:MM] Response initiated
- [HH:MM] Contained
- [HH:MM] Resolved

## Impact
- **Data Exposed:** [What data]
- **Users Affected:** [How many]
- **Financial Loss:** [If any]
- **Reputation Damage:** [Assessment]

## Response Actions
1. [Action 1]
2. [Action 2]
3. [Action 3]

## Root Cause
[What caused the incident]

## Recommendations
1. [Improvement 1]
2. [Improvement 2]
3. [Improvement 3]

## Lessons Learned
[What we learned, how to prevent recurrence]

---
**Reported by:** [Name]
**Date:** [DD MMM YYYY]
**Reviewed by:** [Pengurus/IT]
```

---

## ✅ Security Checklist

### **New User Onboarding:**
```
[ ] Password manager setup (Bitwarden)
[ ] 2FA enabled on all accounts
[ ] Device security verified (lock, encryption, antivirus)
[ ] Security training completed
[ ] Access granted per matrix
[ ] Backup codes stored securely
```

### **Monthly Security Tasks:**
```
[ ] Review login activity (email, social media)
[ ] Check for software updates
[ ] Review antivirus logs
[ ] Verify backups working
[ ] Check phishing attempts (spam folder)
```

### **Quarterly Security Tasks:**
```
[ ] Access review (revoke unnecessary access)
[ ] Password rotation (critical accounts)
[ ] Security policy review
[ ] Incident response drill
[ ] Device security audit
```

### **Annual Security Tasks:**
```
[ ] Full security audit
[ ] Penetration test (if budget allows)
[ ] Backup restoration test
[ ] Disaster recovery drill
[ ] Security training refresh
```

---

## 📞 Support & Resources

| Resource | Link/Contact |
|----------|--------------|
| **IT Support** | timitasib@gmail.com |
| **Bitwarden Setup** | https://bitwarden.com |
| **Google 2FA Setup** | https://support.google.com/accounts/answer/1066447 |
| **Phishing Quiz** | https://phishingquiz.withgoogle.com |
| **Have I Been Pwned** | https://haveibeenpwned.com |
| **Virus Total** | https://www.virustotal.com |
| **Local Police (Cyber Crime)** | [Add local cyber crime unit contact] |

---

**Dokumen ini internal & sensitif — jangan share ke pihak luar**  
**Last reviewed:** 7 Juni 2026  
**Next review:** 7 Desember 2026  
**Access Level:** All members (required reading), IT (implementation)

**Required Acknowledgment:**
```
Saya telah membaca, memahami, dan berkomitmen untuk menerapkan panduan keamanan ini.

Nama: _________________
Role: _________________
Tanggal: _________________
Tanda Tangan: _________________
```