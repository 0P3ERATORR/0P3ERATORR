# 🛡️ Glory | Junior SOC Analyst

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?style=flat&logo=linkedin)](https://www.linkedin.com/in/gloryola)
[![TryHackMe](https://img.shields.io/badge/TryHackMe-Profile-red?style=flat&logo=tryhackme)](https://tryhackme.com/p/Q1ckyBoss)

📧 **Email:** gosecop@proton.me

---

## 👋 About Me

I'm a Junior SOC Analyst focused on identifying, investigating, and responding to security threats through hands-on security operations and continuous technical development.

I have develop practical experience by building security environments and working through realistic analyst scenarios — collecting and analyzing telemetry, investigating suspicious activity, validating detections, remediating security issues, and documenting the evidence and conclusions.

My completed projects span SIEM monitoring and troubleshooting, Windows and Active Directory security, identity and privileged-access monitoring, vulnerability management, and incident investigation. I've worked with technologies including Wazuh, Windows Security Events, Sysmon, PowerShell, Active Directory, Nessus, Linux, and VMware.

I place emphasis on understanding **why** something happened rather than simply producing an alert. That includes tracing events from source to SIEM, analyzing detection logic, troubleshooting failed detections, validating remediation, and documenting limitations when a test does not produce the expected result.

### Core Capabilities

- **Security Operations:** SIEM monitoring · alert triage · log analysis · incident investigation · event correlation
- **Security Monitoring & Detection:** Windows telemetry · authentication monitoring · detection validation · MITRE ATT&CK
- **Identity & Endpoint Security:** Active Directory · privileged-access monitoring · Windows Security Events · Sysmon · PowerShell
- **Vulnerability Management:** Nessus · CVSS · risk prioritization · remediation · hardening · re-scan validation
- **Technical Investigation:** root-cause analysis · evidence collection · troubleshooting · remediation verification
- **Infrastructure:** Windows Server · Windows 11 · Linux · VMware · virtual networking

> **My approach:** Build → Test → Detect → Investigate → Remediate → Verify → Document

🎯 **Career Goal:** Contribute to a Security Operations team while continuing to develop deeper expertise in detection, investigation, threat hunting, and identity security.

---

## Technical Skills & Tools

### 🛡️ SOC & Security Monitoring
Wazuh · SIEM monitoring · alert triage · log analysis · event correlation · incident investigation · MITRE ATT&CK

### 🏢 Active Directory & Identity
Active Directory Domain Services · domain administration · users and security groups · domain-joined endpoints · authentication monitoring · privileged-group monitoring · DNS

### 🖥️ Windows Security
Windows Security Event Logs · Event ID analysis · Sysmon · PowerShell logging · Script Block Logging · process creation auditing · authentication auditing

### ⚙️ Detection & Analysis
Wazuh rule analysis · correlation logic · detection validation · security telemetry analysis · root-cause investigation

### 🔍 Vulnerability Management
Tenable Nessus · CVSS · vulnerability assessment · risk prioritization · remediation · system hardening · re-scan validation

### 🐧 Systems & Infrastructure
Windows Server · Windows 11 · Kali Linux · Ubuntu/Debian · VMware Workstation · virtual networking · systemd

### 🔧 SIEM Troubleshooting
Wazuh Manager · Wazuh Indexer · OpenSearch · Filebeat · agent enrollment · log ingestion · service troubleshooting · indexing analysis

---

# 🔬 Security Projects & Investigations

## 🏢 [Active Directory & Wazuh SOC Monitoring Lab](https://github.com/0P3ERATORR/active-directory-wazuh-soc-lab)

Built an Active Directory security monitoring environment integrating a Windows Server domain controller, domain-joined Windows workstation, Windows Security auditing, and Wazuh SIEM.

The project focused on collecting identity and endpoint telemetry, investigating security events, analyzing Wazuh detection logic, and monitoring privileged Active Directory changes.

### Key Investigations

- Built and validated the `SOCLAB.LOCAL` Active Directory environment
- Joined a Windows workstation to the domain and validated domain authentication
- Deployed and enrolled Wazuh agents for endpoint and domain-controller monitoring
- Monitored process creation using **Windows Event ID 4688**
- Investigated failed authentication using **Event ID 4625** and **Wazuh Rule 60122**
- Analyzed **Wazuh Rule 60204** correlation logic for multiple Windows logon failures
- Documented why Rule 60204 did not trigger under the specific local test conditions instead of reporting an unsupported detection
- Monitored security-group membership changes using **Event IDs 4728 and 4729**
- Simulated a controlled privileged-group modification by temporarily adding a test account to **Domain Admins**
- Detected the privileged modification using **Wazuh Rule 60159 — Level 12 "Domain Admins Group Changed"**
- Removed the temporary privileged membership and verified remediation
- Produced a full technical report containing architecture, evidence, investigations, troubleshooting, remediation, and detection analysis

### Detection Highlight

`Domain Admins modification → Event 4728 → DC01 → Wazuh → Rule 60159 → Level 12 alert → Investigation → Remediation`

**Technologies:** Active Directory · Windows Server · Windows 11 · Wazuh · Windows Security Events · PowerShell · VMware

---

## 🛡️ [Wazuh SOC Detection & Investigation Lab](https://github.com/0P3ERATORR/wazuh-soc-detection-lab)

Built an isolated SOC/SIEM environment using Wazuh and Windows to collect security telemetry, validate detections, investigate alerts, and troubleshoot failures across the SIEM pipeline.

### Key Investigations

- Investigated Windows authentication activity and correlated **Event ID 4625 with Event ID 4624**
- Detected Windows account creation using **Event ID 4720** and **Wazuh Rule 60109**
- Collected and analyzed PowerShell Script Block Logging using **Event ID 4104**
- Investigated Wazuh alerts mapped to MITRE ATT&CK techniques including **T1098, T1059.001, T1112, and T1531**
- Investigated endpoint events from source telemetry through SIEM ingestion and alert generation
- Troubleshot Wazuh Indexer OOM failures
- Diagnosed Filebeat connectivity and indexing issues
- Investigated service startup failures and SIEM indexing delays
- Documented investigation methodology, root-cause analysis, remediation, and verification

**Technologies:** Wazuh · Windows · Windows Event Logs · PowerShell · Sysmon · MITRE ATT&CK · Linux

---

## 🔍 [Metasploitable2 Vulnerability Management Lab](https://github.com/0P3ERATORR/Metasploitable2-vulnerability-management-lab)

Performed a complete vulnerability-management lifecycle against a deliberately vulnerable Linux system.

### Workflow

`Identify → Assess → Prioritize → Remediate → Verify`

Four Critical/High findings were addressed, including remediation of the **CVSS 9.8 Ghostcat vulnerability (CVE-2020-1938)**.

### Key Work

- Conducted vulnerability scanning and assessment using Tenable Nessus
- Prioritized findings using severity and CVSS information
- Investigated affected services and configurations
- Remediated weak credentials
- Hardened Apache Tomcat AJP configuration
- Addressed SSL/TLS weaknesses
- Hardened NFS exports
- Performed independent re-scans after remediation
- Compared before-and-after scan results to verify remediation
- Documented technical evidence and remediation outcomes

**Technologies:** Tenable Nessus · Linux · CVSS · Apache Tomcat · SSL/TLS · NFS · VMware

---

## 🖥️ [Cybersecurity Home Lab](https://github.com/0P3ERATORR/Cybersecurity-home-lab)

Built and maintained the virtualized infrastructure used to support my cybersecurity projects.

The environment provides isolated systems for security monitoring, vulnerability assessment, Active Directory, Windows analysis, and Linux-based security work.

### Environment & Experience

- VMware-based virtualization
- Isolated virtual networking
- Windows and Linux systems
- Kali Linux attack/testing environment
- Windows security tooling
- Security monitoring infrastructure
- Resource allocation and optimization
- Network troubleshooting
- Software compatibility troubleshooting
- Security-tool deployment

The lab has also provided practical experience troubleshooting memory constraints, disk limitations, networking problems, service failures, and software compatibility issues.

**Technologies:** VMware Workstation · Windows · Windows Server · Kali Linux · Linux · virtual networking

---

# 🗺️ Security Project Roadmap

My next projects are designed to broaden my exposure to common SOC workflows while building on the investigation and monitoring skills demonstrated in my completed labs.

## 🎣 Phishing Investigation

**Focus:**  
Email header analysis · sender investigation · IOC extraction · URL/domain analysis · threat intelligence enrichment · analyst disposition · incident reporting

**Goal:**  
Develop a documented end-to-end workflow for investigating suspicious email activity and determining whether an email should be classified as malicious, suspicious, or benign.

---

## 🕵️ Threat Hunting

**Focus:**  
Hypothesis-driven hunting · Windows telemetry · authentication activity · MITRE ATT&CK · investigative queries · detection gaps

**Goal:**  
Move beyond alert-driven investigation by developing hypotheses and proactively searching available telemetry for suspicious behavior.

---

## 🐍 SOC Automation with Python

**Focus:**  
Python · APIs · IOC enrichment · log parsing · automation · security workflows

**Goal:**  
Automate repetitive analyst tasks such as IOC processing, enrichment, log parsing, and security-data handling.

---

## 🔐 Secure Communications & PKI Security

**Focus:**  
PKI · TLS · digital certificates · certificate chains · OpenSSL · certificate validation · secure communications

**Goal:**  
Develop practical knowledge of how certificates, trust chains, encryption, and secure communications are implemented and investigated.

---

## 🐧 Linux Hardening & Security Monitoring

**Focus:**  
Linux authentication · permissions · auditd · system hardening · log analysis · security monitoring

**Goal:**  
Develop stronger Linux defensive-security skills through system hardening, auditing, telemetry collection, and investigation.

---

# 📈 Project Progress

### ✅ Completed

- [x] 🖥️ Cybersecurity Home Lab
- [x] 🔍 Vulnerability Management & Remediation Lab
- [x] 🛡️ Wazuh SOC Detection & Investigation Lab
- [x] 🏢 Active Directory & Wazuh SOC Monitoring Lab

### 🔜 Upcoming

- [ ] 🎣 Phishing Investigation
- [ ] 🕵️ Threat Hunting
- [ ] 🐍 SOC Automation with Python
- [ ] 🔐 Secure Communications & PKI Security
- [ ] 🐧 Linux Hardening & Security Monitoring

---

## 🎯 Current Goals

- Continue developing practical SOC investigation experience
- Build an end-to-end phishing investigation workflow
- Develop hypothesis-driven threat-hunting skills
- Build and validate additional security detections
- Automate repetitive security-analysis tasks using Python
- Expand my understanding of identity and authentication security
- Develop practical knowledge of PKI, TLS, and certificates
- Strengthen Linux defensive-security and monitoring skills
- Earn CompTIA Security+
- Secure my first professional SOC / Security Analyst role

---

## 🤝 Let's Connect

I'm open to networking, feedback, collaboration, and entry-level opportunities in **SOC, blue team, security operations, and security engineering**.

- 💼 **LinkedIn:** [linkedin.com/in/gloryola](https://www.linkedin.com/in/gloryola)
- 🧪 **TryHackMe:** [tryhackme.com/p/Q1ckyBoss](https://tryhackme.com/p/Q1ckyBoss)
- 📧 **Email:** gosecop@proton.me
