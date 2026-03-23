# Enterprise Hybrid Cloud & Endpoint Security Lab
**A Microsoft 365 & Intune Administration Portfolio**

## 📌 Project Overview
This project demonstrates the design, deployment, and management of a secure, scalable Microsoft 365 environment. It simulates a mid-sized corporate infrastructure focusing on Zero-Trust security, automated device compliance, and structured IT support workflows.

## 🛠️ Tech Stack & Tools
* **Identity:** Microsoft Entra ID (Formerly Azure AD)
* **MDM/UEM:** Microsoft Intune (Endpoint Manager)
* **Security:** BitLocker, MFA, Conditional Access, RBAC
* **OS:** Windows 11 Enterprise (Virtualized)
* **Collaboration:** Microsoft Teams, SharePoint Online

---

## 🚀 Key Projects (PAR Method)

### 1. Enterprise Identity & Access Management (IAM)
* **Problem:** Lack of a structured user hierarchy led to "over-permissioning" and inefficient onboarding.
* **Action:** Provisioned 25 unique identities with departmental metadata. Implemented **Role-Based Access Control (RBAC)** by delegating "Helpdesk Administrator" roles to technical leads.
* **Result:** Established a scalable identity foundation ensuring the **Principle of Least Privilege**, reducing administrative overhead.
* *📸 View evidence in `/screenshots/active-users.png`*

### 2. Phased Endpoint Compliance Rollout (Change Management)
* **Problem:** Unmanaged workstations accessing corporate data without encryption posed a high security risk.
* **Action:** Developed an Intune Compliance Policy (BitLocker, Secure Boot, 8-char alphanumeric password). To mitigate downtime, I utilized a **Pilot Security Group (`SEC-Intune-Pilot`)** for initial testing before tenant-wide deployment.
* **Result:** Achieved 100% visibility into device health and automated the blocking of non-compliant hardware.
* *📸 View evidence in `/screenshots/pilot-group.png`*

### 3. Real-World Security Remediation
* **Problem:** A test device (User: Amita Sharma) was flagged as "Non-Compliant" due to a weak 4-digit PIN.
* **Action:** Monitored the Intune dashboard, performed a manual MDM sync on the client VM, and enforced a password update to meet corporate standards.
* **Result:** Successfully transitioned the device from **"Not Evaluated"** to **"Compliant,"** restoring secure access to SaaS applications.
* *📸 View evidence in `/screenshots/compliance-success.png`*

### 4. Structured Helpdesk & Collaboration Infrastructure
* **Problem:** Fragmented communication for technical issues delayed Tier 1 response times.
* **Action:** Deployed a **Microsoft Teams Helpdesk** with dedicated channels (`TEAM-All-Staff`, `TEAM-HR-Internal`) and configured specific security groups for restricted folder access.
* **Result:** Centralized user requests and established a clear escalation path for the IT team.

---

## 📈 Lab Architecture & Governance
* **User Provisioning:** 25 users across HR, Finance, and IT departments.
* **Security Groups:** * `SEC-M365-Admins`: Privileged access for administrative accounts.
    * `SEC-Intune-Pilot`: Change management testing group.
    * `SEC-Finance-Access`: Department-specific resource locking.

## 📁 Repository Structure
```text
├── README.md              <-- (You are here)
├── /documentation         <-- Full PDF version of the portfolio
├── /screenshots           <-- Proof of compliance and configurations
│   ├── active-users.png
│   ├── pilot-group.png
│   ├── compliance-success.png
│   └── teams-infrastructure.png
