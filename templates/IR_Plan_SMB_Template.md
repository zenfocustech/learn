lan

**Organization:** [Company Name] **Plan Owner (IR Lead):** [Name/Title] **Version:** [1.0] **Last Reviewed:** [Date] **Next Review Due:** [Date, at least annually] **Governing Policy:** Incident Response Policy

> **Keep a printed copy of Sections 1 and 2 in a known location. If email and systems are down, you still need this.**

---

## 1. Quick Start: First 60 Minutes

**If you suspect an incident, do these in order:**

1. **Report it.** Contact the IR Lead at [phone/email]. If there's no answer in [15 minutes], call the Backup Lead at [phone].
2. **Don't make it worse.** Do not delete files, wipe or reboot devices, or log in to affected accounts to "look around." Disconnect the affected device from the network (unplug the cable or turn off Wi-Fi). Leave it powered on unless told otherwise.
3. **Write it down.** Note the time, what you saw, and what you did.
4. **IR Lead takes over.** The IR Lead opens an incident log entry, classifies severity (Section 5), and starts the response.
5. **Call for help** if severity is Medium or higher: IT/security provider, then insurance carrier (Section 2).
6. **Say nothing externally.** Do not discuss the incident with customers, vendors, or on social media. The Communications Contact handles that.

---

## 2. Contact Sheet

_Review quarterly. Keep a printed copy and an offline copy (for example, on a phone)._

|Who|Name|Phone (24/7)|Email|
|---|---|---|---|
|IR Lead||||
|Backup IR Lead||||
|Executive Sponsor||||
|Communications Contact||||
|IT / MSP / MSSP||||
|Cyber Insurance Carrier (claims hotline)|||Policy #:|
|Legal Counsel||||
|Bank / Payment Processor||||
|Key Software/Cloud Vendors (email, accounting, etc.)||||
|Local FBI Field Office / IC3.gov||||
|State Attorney General (breach reporting)||||
|Regulator or Customer Contacts (if contractually required)||||

---

## 3. Roles During an Incident

|Role|Duties|
|---|---|
|**IR Lead**|Declares the incident. Sets severity. Directs response. Assigns tasks. Maintains the log. Briefs the Executive Sponsor.|
|**Executive Sponsor**|Makes business decisions, such as taking systems offline, paying for outside help, and approving notifications. Has final authority.|
|**IT / Security Provider**|Investigates, contains, removes the threat, restores systems, and preserves evidence.|
|**Communications Contact**|Drafts and delivers all approved messages to staff, customers, and media.|
|**Legal Counsel**|Advises on notification duties, privilege, and contracts. Engaged by the Executive Sponsor or IR Lead.|
|**All Staff**|Report, follow instructions, and preserve evidence.|

_For very small teams, one person may hold several roles. Just make sure each role has a named backup._

---

## 4. What We're Protecting

_Complete this once, then update annually. It lets you decide quickly what matters most. Choice follows visibility._

|Critical System / Data|Where It Lives|Owner|Max Acceptable Downtime|Backup Location / Last Tested|
|---|---|---|---|---|
|Email|[M365 / Google]||||
|Financial / accounting|||||
|Customer data / CRM|||||
|File storage|||||
|Line-of-business application|||||
|Payment systems|||||
|Website|||||

**Also record:** where the admin credentials are stored (offline and secure), who holds MFA recovery methods, and where the network diagram or asset list is kept.

---

## 5. Severity Levels

|Level|Description|Examples|Response|
|---|---|---|---|
|**Low**|Contained, no data exposure, minimal disruption|Blocked phishing email, single malware detection stopped by antivirus|IR Lead logs and handles. Review at the next check-in.|
|**Medium**|Possible exposure or disruption to a user or system|One compromised email account, lost laptop (encrypted), suspicious login|IR Lead engages IT provider same day. Notify the Executive Sponsor.|
|**High**|Confirmed data exposure, multiple systems affected, or business operations impacted|Ransomware, business email compromise with financial loss, unencrypted device with customer data lost, confirmed data theft|Immediate response. Activate Executive Sponsor, IT provider, insurer, and legal counsel.|

**When unsure, rate it higher and downgrade later.**

---

## 6. Response Phases

### 6.1 Preparation (Ongoing)

- Keep this plan and the contact sheet current.
- Maintain tested backups, including at least one offline or immutable copy.
- Enforce MFA, patching, and endpoint protection.
- Enable logging on email, cloud, and critical systems so there's something to investigate.
- Train all staff annually on recognizing and reporting incidents.
- Confirm cyber insurance terms, including notice deadlines and required or approved vendors.

### 6.2 Identification and Analysis

The IR Lead, with the IT provider, will:

- Confirm whether an actual incident occurred.
- Determine what happened, which systems and data are involved, and when it started.
- Assign a severity level (Section 5).
- Decide whether regulated or customer data may be involved. This drives notification in Section 7.
- Open the incident log (Section 9).

### 6.3 Containment

**Short-term (stop the spread):**

- Isolate affected devices from the network.
- Disable compromised accounts and reset passwords and sessions. Revoke MFA tokens where needed.
- Block malicious senders, IPs, or domains.
- Take affected systems offline if needed. The IR Lead may do this, and the Executive Sponsor is informed immediately.

**Evidence:** Do not wipe or rebuild systems until the IT provider confirms evidence has been preserved (disk images, logs, screenshots, original emails). Record who handled what, and when.

### 6.4 Eradication

- Remove malware, unauthorized accounts, and malicious forwarding rules or access.
- Close the way in: patch the vulnerability, fix the misconfiguration, or remove the unauthorized access.
- Verify the threat is gone before restoring.

### 6.5 Recovery

- Restore from known-clean backups.
- Rebuild affected systems where trust is lost.
- Reset all credentials that may have been exposed.
- Monitor closely for [30] days for signs of re-entry.
- Return to normal operations only with the IR Lead's approval.

### 6.6 Lessons Learned

Within [30] days of closing a Medium or High incident, hold a review with everyone involved:

- What happened and how did we find out?
- What worked? What didn't?
- What should change in our controls, training, or this plan?
- Assign each action an owner and a due date. Update this plan.

---

## 7. Notification and Communication

**Decision owner:** The Executive Sponsor, with Legal Counsel.

**Check these obligations at every Medium or High incident:**

- [ ] **Cyber insurance:** notify the carrier per policy terms (often immediately)
- [ ] **State breach notification laws** (customers' state of residence): many require notice if personal information may have been exposed
- [ ] **Customer contracts:** many set specific notice deadlines
- [ ] **Industry or regulatory rules:** [HIPAA, PCI DSS, CMMC/DFARS, FTC Safeguards, etc., as applicable]
- [ ] **Law enforcement:** report to the FBI IC3 or local authorities for fraud, extortion, or theft
- [ ] **Bank / payment processor:** immediately, if funds or payment data are involved

**Message rules:**

- One voice: the Communications Contact.
- Facts only. Don't speculate on cause, fault, or scope.
- Have Legal Counsel review outside statements.
- Keep staff informed on a need-to-know basis, using a channel that isn't compromised (phone, text, or personal email if company email is affected).

**Ransomware:** Do not pay or contact the attackers without Executive Sponsor, Legal Counsel, and insurer involvement.

---

## 8. Scenario Cheat Sheets

_One page each. Add more over time._

**Phishing / compromised email account**

1. Reset the password and revoke active sessions.
2. Check for forwarding rules, inbox rules, and newly added MFA devices.
3. Review sign-in logs and sent mail.
4. Warn recipients of any malicious messages sent.
5. If money was requested or moved, call the bank immediately.

**Ransomware / malware**

1. Disconnect affected devices from the network. Do not power off unless told to.
2. Isolate backups so they can't be reached.
3. Call the IT provider and insurer.
4. Identify the scope and the variant.
5. Restore from clean backups after eradication.

**Lost or stolen device**

1. Report immediately.
2. Remotely lock or wipe the device.
3. Confirm whether it was encrypted and what data it held.
4. Reset the user's credentials.
5. Assess notification duties.

**Business email compromise / wire fraud**

1. Call the bank immediately and request a recall.
2. Report to IC3.gov.
3. Preserve the emails.
4. Notify the insurer.

**Unauthorized access / data exposure**

1. Identify what was accessed.
2. Close the access.
3. Preserve logs.
4. Engage Legal Counsel on notification.

---

## 9. Incident Log

_Use for every incident, even Low ones. Keep it with restricted access._

|Field|Entry|
|---|---|
|Incident #||
|Date/time discovered||
|Reported by||
|Description||
|Systems / data affected||
|Severity||
|Actions taken (with times and who)||
|Evidence preserved (what and where)||
|Notifications made (who, when, how)||
|Date contained / recovered / closed||
|Root cause||
|Lessons learned / follow-up actions (owner, due date)||

---

## 10. Testing and Maintenance

|Activity|Frequency|Owner|Last Done|
|---|---|---|---|
|Tabletop exercise (walk through a scenario)|Annually, at minimum|IR Lead||
|Contact sheet verification|Quarterly|IR Lead||
|Backup restore test|[Quarterly]|IT Provider||
|Staff awareness training|Annually, plus onboarding|[HR / IR Lead]||
|Plan review and update|Annually and after every High incident|IR Lead||
|Insurance policy review|Annually|Executive Sponsor||

Testing the plan is part of operating an IR capability, not an optional extra. Plans that aren't practiced tend to fail when they're needed.

---

## 11. Approval

Approved by: 
Title: 
Date:
