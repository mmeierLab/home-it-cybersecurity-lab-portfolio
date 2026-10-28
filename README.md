# Home IT & Cybersecurity Lab Portfolio

A hands-on personal lab documenting practical work in IT support, Windows administration, identity and access management, network troubleshooting, service-desk workflows, and security monitoring.

**[Open the full technical portfolio (PDF)](Home_IT_Cybersecurity_Lab_Portfolio.pdf)**

The portfolio describes the lab architecture, selected troubleshooting cases, 12 GLPI tickets, the Northstar Services Active Directory and access-control project, Wazuh event analysis, and the observed results and limits of each exercise.

## Lab overview

The environment uses VMware Workstation Pro to run a small, isolated virtual lab with Windows Server/Active Directory, a Windows client, a Linux system hosting GLPI, and a Wazuh monitoring stack. The project focuses on repeatable steps: establish a baseline, make a controlled change, test the result, record evidence, and distinguish verified outcomes from unresolved questions.

## Technologies and tools

- **Virtualization:** VMware Workstation Pro
- **Windows administration:** Windows Server 2025, Windows 11, Active Directory Domain Services (AD DS), DNS, Group Policy, Windows services, and Windows event logs
- **Identity and access management:** Organizational units, user provisioning, security-group membership, account lifecycle administration, NTFS permissions, SMB share permissions, and group-based access testing
- **Networking:** IPv4, DNS, DHCP, VMware virtual networking, and connectivity troubleshooting
- **Service desk:** GLPI ticketing, incident investigation, troubleshooting notes, remediation records, and verification
- **Security monitoring:** Wazuh SIEM and Windows security-event analysis
- **Linux services:** Foundational command-line and service troubleshooting

## Selected projects

### Northstar Services — Active Directory and group-based access control

Created a fictional organization with 25 synthetic employee accounts across five departments and five departmental Global Security groups. Configured departmental folders with matching NTFS permissions and SMB share access. For one designated employee per department, verified access and test-file creation in that employee's own share and recorded a selected cross-department access attempt that did not open its target share. The exercise demonstrates an RBAC-style model; not every account and every possible share combination was tested.

### GLPI service-desk case studies

Documented 12 tickets involving controlled account-administration and support scenarios, including password changes, file permissions, DNS, Apache service recovery, Windows services, Group Policy, firewall-rule investigation, and Linux file permissions. The portfolio distinguishes administrative ticket closure from technical verification where those outcomes differ.

### Wazuh security monitoring

Investigated Windows events in Wazuh. Verified examples include failed-logon Event ID 4625 (Wazuh rule 60122) and local-account creation Event ID 4720 (rule 60109). Other attempts are identified separately where expected telemetry or a specific rule match was not established. The portfolio does not claim that Northstar events were detected by Wazuh or that a complete Wazuh-to-GLPI response workflow was demonstrated.

### Network troubleshooting

Documented a VMware VMnet1 host-only networking issue in which disabled DHCP caused the Windows client to receive an APIPA address and fail to reach the Wazuh endpoint. Re-enabling VMnet1 DHCP restored valid client addressing, successful connectivity, and an active Wazuh agent.

## Repository contents

- `README.md` — this overview
- `Home_IT_Cybersecurity_Lab_Portfolio.pdf` — full technical portfolio with selected visual evidence

## Scope and accuracy

This is a personal learning and demonstration environment, not a production enterprise. The portfolio describes work at the level supported by the recorded evidence and identifies material verification limitations. Northstar Services is fictional; its employee accounts are synthetic.

Before making this repository public, review the portfolio and any future screenshots for passwords, tokens, private keys, personal information, and infrastructure details you do not want to publish. Never commit credentials or secrets to the repository.
