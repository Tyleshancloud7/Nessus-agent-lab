<p align="center">
  <img src="https://img.shields.io/badge/Security-Vulnerability%20Management-blue?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Tool-Tenable%20Nessus-purple?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Focus-Agent%20Based%20Scanning-red?style=for-the-badge"/>
</p>

<h1 align="center">🛡️ Nessus Agent Deployment Lab</h1>

<p align="center">
Deploying and validating a Tenable Nessus Agent on a Windows 11 virtual machine to simulate a real vulnerability management workflow.
</p>

---

# 🎯 Project Overview

This project documents the **deployment and configuration of a Tenable Nessus Agent** on a Windows 11 virtual machine.

The objective was to simulate how security teams deploy **agent-based vulnerability scanning** in enterprise environments.

Unlike network scans, agent-based scanning allows organizations to:

* Detect vulnerabilities on remote or roaming devices
* Perform authenticated scanning
* Improve visibility into endpoint security posture

This lab required **three days of troubleshooting, configuration, and validation**, reflecting the real-world challenges security teams face during vulnerability management deployments.

---

# 🧠 Real-World Scenario

A security operations team needs to deploy **vulnerability monitoring across employee endpoints**.

Because many devices operate remotely or outside the corporate network, traditional network scanning cannot reliably detect vulnerabilities.

The organization therefore deploys **Tenable Nessus Agents** to endpoints to ensure:

* Continuous vulnerability monitoring
* Authenticated system assessment
* Secure agent communication with the Tenable cloud platform

This project demonstrates how a **Security Analyst or Vulnerability Management Engineer** would deploy and validate this system.

---

# 🖥️ Lab Environment

| Component         | Details            |
| ----------------- | ------------------ |
| Virtual Machine   | `Tyl-Win11`        |
| Operating System  | Windows 11         |
| Platform          | Tenable Cloud      |
| Scan Type         | Basic Agent Scan   |
| Trigger Mechanism | File-based trigger |
| Trigger File      | `start.txt`        |

---

# ⚙️ Deployment Workflow

## 1️⃣ Provision Windows 11 Virtual Machine

* Created a new Windows 11 VM
* Configured secure credentials
* Verified successful boot and OS functionality
* Documented VM identifier: `Tyl-Win11`

---

## 2️⃣ Create Agent Group

Navigation:

Settings → Sensors → Nessus Agents → Agent Groups → **Add Agent Group**

Actions performed:

* Created a dedicated **agent group**
* Prepared group for endpoint enrollment

Agent groups allow security teams to **organize devices and assign scans at scale**.

---

## 3️⃣ Configure Basic Agent Scan

Created a new scan using:

Scan Type → **Basic Agent Scan**

Configured parameters:

* Target agent group
* Scan policy
* Trigger-based execution

Trigger file configured as:

`start.txt`

---

## 4️⃣ Install Tenable Nessus Agent

Installation steps:

1. Logged into the Windows VM
2. Accessed the Tenable Cloud portal
3. Navigated to:

Settings → Sensors → Nessus Agents → **Add Nessus Agent**

4. Copied the **PowerShell installation command**
5. Modified command parameters:

   * Custom agent name
   * Correct agent group assignment
6. Opened **PowerShell as Administrator**
7. Executed installation command

The agent successfully registered with the Tenable platform.

---

## 5️⃣ Trigger the Scan

To start the scan:

1. Created file:

`start.txt`

2. Placed file inside the configured trigger directory
3. Observed file deletion

File deletion indicates the **scan trigger was successfully processed**.

---

## 6️⃣ Verify Agent and Scan Results

Verification process:

Navigation:

Settings → Sensors → Nessus Agents

Confirmed:

* Agent `Tyl-Win11` successfully linked

Next:

Scans → **See All Details**

Observed:

* Vulnerabilities populating
* Scan results updating

Typical population time: **30–60 minutes**

---

## 🧹 Cleanup (Operational Hygiene)

To maintain a clean environment:

* Deleted scan configuration
* Deleted agent group
* Unlinked agent
* Deleted Windows virtual machine

Security labs should always end with **environment cleanup and resource removal**.

---

# 📊 Vulnerability Management Workflow

This lab demonstrates a standard **enterprise vulnerability management lifecycle**:

1️⃣ Asset provisioning
2️⃣ Agent deployment
3️⃣ Endpoint registration
4️⃣ Vulnerability scanning
5️⃣ Results analysis
6️⃣ Environment cleanup

---

# 🛠 Skills Demonstrated

* Vulnerability Management
* Tenable Nessus Agent Deployment
* Endpoint Security Monitoring
* Virtual Machine Administration
* PowerShell Execution
* Security Troubleshooting
* Scan Configuration and Validation

---

# 🔐 Security Best Practices

Weak credentials remain one of the most common causes of system compromise.

Never deploy systems with credentials such as:

Username: `admin`
Password: `letmein123`

Instead:

* Use strong passwords
* Use unique credentials
* Rotate credentials regularly

---

# 💡 Why Agent-Based Scanning Matters

Agent-based scanning solves several limitations of traditional vulnerability scans:

* Works on remote devices
* Enables authenticated vulnerability detection
* Provides continuous monitoring
* Improves visibility for distributed workforces

These capabilities make agent scanning a **critical component of modern vulnerability management programs**.

---

# 💭 Final Thoughts

This lab required multiple rounds of troubleshooting:

* Agent linking delays
* Trigger configuration issues
* Scan execution verification

Real cybersecurity work rarely functions perfectly on the first attempt.

Success comes from **persistence, investigation, and iterative problem solving**.

And now?

The agent is deployed.
The scan runs.
The vulnerabilities surface.

Welcome to vulnerability management.
