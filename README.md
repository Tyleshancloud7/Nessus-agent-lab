# Nessus-agent-lab
# 🛡️ Nessus Agent Deployment Lab – Windows 11 (Tyl-Win11)

> ⚠️ IMPORTANT: Use `start.txt` as your trigger file.  
> Not `dishsoap.lol`. We don’t talk about that decision.

---

## 🎯 Project Overview

This project documents my full deployment of a **Tenable Nessus Agent** on a Windows 11 Virtual Machine (`Tyl-Win11`).

This lab took me **3 days to complete** due to troubleshooting, configuration issues, and learning how agent-based scanning actually works in a real environment.

No shortcuts.  
No default passwords.  
No quitting.

---

## 🖥️ Environment Details

- VM Name: `Tyl-Win11`
- Operating System: Windows 11
- Platform: Tenable Cloud
- Scan Type: Basic Agent Scan (Triggered)
- Trigger File: `start.txt`

---

## 🔐 Security Reminder

Do NOT use weak credentials.

Example of what NOT to use:

Username: hackerwannabe  
Password: letmein123  

If a VM stays online long enough with weak credentials, it will get breached.

Always use strong, unique credentials.

---

# ⚙️ Steps I Completed

---

## 1️⃣ Provisioned Windows 11 Virtual Machine

- Created a brand new Windows 11 VM
- Created secure credentials (no defaults, no easy passwords)
- Verified VM boot and system stability
- Took note of VM name: `Tyl-Win11`

---

## 2️⃣ Created Agent Group

Navigation:

Settings → Sensors → Nessus Agents → Agent Groups → + Add Agent Group

- Created a new agent group for this deployment

---

## 3️⃣ Created Basic Agent Scan

- Created new scan
- Selected scan type: Basic Agent Scan
- Selected the agent group created earlier
- Configured scan as **Triggered Scan**
- Set trigger filename as:

`start.txt`

---

## 4️⃣ Provisioned Tenable Agent

Steps completed:

- Logged into Windows VM with secure credentials
- Logged into Tenable Cloud portal
- Navigated to:

Settings → Sensors → Nessus Agents → + Add Nessus Agent

- Copied PowerShell installation command
- Edited command in Notepad to:
  - Set custom agent name
  - Assign correct agent group
- Opened PowerShell as Administrator
- Executed installation command
- Verified successful installation

---

## 5️⃣ Triggered the Scan

- Created file named `start.txt` in the configured trigger directory
- Observed the file disappear
  - This confirms the scan started
- Returned to Tenable portal to monitor agent status

---

## 6️⃣ Verified Agent Link & Scan Results

- Navigated to:
  Settings → Sensors → Nessus Agents
- Confirmed my agent (`Tyl-Win11`) appeared in portal
- Waited 30–60 minutes for vulnerabilities to populate
- Navigated to:
  Scans → See All Details
- Reviewed vulnerability results

---

## 7️⃣ Cleanup (Operational Hygiene)

- Deleted scan
- Deleted agent group
- Unlinked agent
- Deleted virtual machine

Because real-world cybersecurity includes cleanup.

---

# 🔥 What This Project Demonstrates

- Vulnerability management workflow
- Secure VM provisioning
- Agent-based scanning configuration
- Trigger-based scan execution
- Real troubleshooting under pressure
- Persistence

---

# 💭 Final Thoughts

This lab took me 3 days.

Multiple configuration issues.  
Agent linking delays.  
Trigger mistakes.  

But no quitting.

Cybersecurity isn’t about knowing everything.

It’s about staying in the fight long enough to figure it out.

And now?

I’m in range.
