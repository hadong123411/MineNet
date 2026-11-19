# MineNet
### Cloud-Based Enterprise Cybersecurity & AI Security Operations Lab

| Project Information | Details |
|---------------------|---------|
| **Project Status** | Planning & Architecture Design |
| **Version** | 1.0 |
| **Development Timeline** | 3 months (initial implementation) |
| **Project Type** | Independent Cybersecurity Engineering Portfolio Project |

---

## 1. Project Overview

MineNet is an independently designed, cloud-based enterprise cybersecurity laboratory that simulates a modern corporate IT environment.

The project aims to demonstrate practical skills in enterprise network architecture, cloud infrastructure, identity and access management, security monitoring, threat detection, incident response, and AI-assisted cybersecurity operations.

MineNet will integrate traditional enterprise networking concepts with cloud technologies, providing a controlled environment for security engineering and testing.

A key feature of the project is the integration of two AI-assisted systems:

- **Offensive AI:** Conducts controlled security tests against authorised infrastructure.
- **Defensive AI:** Analyses security telemetry, investigates threats, and executes limited autonomous defensive responses through a restricted policy engine.

The initial implementation will be developed over three months. The infrastructure will be designed for future expansion, allowing the environment to be archived, restored, and extended over time.

---

## 2. Project Objectives

**The primary objectives of MineNet are to:**

1. Design and deploy a simulated enterprise infrastructure in the cloud.
2. Implement secure network segmentation across multiple departments.
3. Configure enterprise routing, firewall policies, NAT, and VPN connectivity.
4. Deploy Active Directory for centralised identity and access management.
5. Establish a Security Operations Centre using industry-relevant monitoring technologies.
6. Develop controlled AI-assisted attack simulation capabilities.
7. Build an AI-assisted defensive system with limited autonomous response capabilities.
8. Evaluate detection accuracy, response effectiveness, and network security controls.
9. Implement backup, recovery, and infrastructure automation.
10. Produce professional technical documentation and reproducible deployment configurations.

---

## 3. Enterprise Architecture

MineNet will simulate an organisation consisting of five departments.

| Department | Primary Function |
|---|---|
| IT | Infrastructure administration and technical support |
| Human Resources | Employee information and access management |
| Finance | Financial operations and sensitive data |
| Operations | Business operations and internal services |
| Cybersecurity / SOC | Threat monitoring, investigation, and incident response |

Each department will operate within a logically separated network.

Shared infrastructure services will be hosted in dedicated security zones to reduce unnecessary duplication and support centralised administration.

### Planned Network Components

- Microsoft Azure virtual networking (proposed)
- OPNsense virtual firewall
- Departmental subnets
- Azure route tables and Network Security Groups
- Centralised internet access and NAT
- WireGuard remote-access VPN
- Active Directory and DNS
- Dedicated management and security networks
- DMZ containing a secure web application
- Isolated testing environment for vulnerable applications

The architecture will support future expansion without requiring a complete redesign.

---

## 4. Security Monitoring and Detection

MineNet will implement centralised security monitoring using several complementary technologies.

| Technology | Purpose |
|---|---|
| Wazuh | SIEM, security event analysis, and endpoint monitoring |
| Sysmon | Detailed Windows system activity logging |
| Suricata | Network intrusion detection and traffic inspection |
| OPNsense | Firewall enforcement, routing, and security logging |
| Python | Custom security automation and AI integrations |

### Planned Detection Capabilities

- Authentication attack detection
- Suspicious process execution
- Network reconnaissance detection
- Unauthorised access monitoring
- Network segmentation violation detection
- File integrity monitoring
- Vulnerability monitoring
- Firewall event correlation
- Security alert investigation

Custom detection rules and monitoring configurations will be developed and tested throughout the project.

---

## 5. AI-Assisted Offensive Security

MineNet will include an AI-assisted offensive security component designed to conduct controlled security testing against authorised laboratory infrastructure.

**The offensive system will:**

- Operate within a restricted testing environment.
- Identify approved testing targets.
- Select techniques from a predefined set of authorised actions.
- Execute controlled security tests.
- Analyse results and determine appropriate subsequent tests.
- Record activities for evaluation and documentation.

All testing will remain restricted to the MineNet environment.

The objective is to evaluate the effectiveness of defensive monitoring and incident response capabilities.

---

## 6. AI-Assisted Defensive Security

The defensive AI will integrate with Wazuh through a custom Python application.

### Planned Workflow

1. Security monitoring tools collect endpoint and network telemetry.
2. Wazuh processes security events and generates alerts.
3. The Python application forwards relevant alert information to a cloud-hosted AI API.
4. The AI analyses security evidence and proposes defensive actions.
5. A deterministic policy engine validates the proposed response.
6. Approved, low-risk actions are executed through restricted response integrations.
7. Actions are verified, logged, and reversed when appropriate.

### Autonomous Response Safeguards

- Preapproved response actions
- Restricted execution permissions
- Protected management infrastructure
- Temporary and reversible responses
- Action logging and auditing
- Human approval for higher-risk actions
- Emergency shutdown capability

The defensive system will be evaluated against conventional rule-based detection and response mechanisms.

---

## 7. Enterprise Services

MineNet will include shared enterprise services to support realistic security scenarios.

| Service | Planned Technology |
|---|---|
| Identity Management | Windows Server Active Directory |
| DNS | Windows Server DNS |
| File Sharing | SMB and NTFS permissions |
| Database | PostgreSQL |
| Cloud Backup | Azure Backup |
| Application Backup | Restic |
| Infrastructure Automation | Terraform and Ansible |

These services will support authentication, authorisation, network security, access-control testing, and disaster recovery exercises.

---

## 8. Technology Stack

### Cloud and Infrastructure
- Microsoft Azure (proposed)
- Windows Server
- Ubuntu Linux
- Terraform
- Ansible

### Networking
- OPNsense
- WireGuard
- Azure Virtual Networks
- Network Security Groups
- Routing and NAT

### Cybersecurity
- Wazuh
- Sysmon
- Suricata
- Custom detection rules
- Security event correlation

### AI and Development
- Python
- Cloud-hosted AI API
- Custom policy engine
- Security automation scripts
- REST API integrations

### Applications and Data
- PostgreSQL
- Nginx
- Flask
- Docker

---

## 9. Development Roadmap

### Month 1 — Enterprise Infrastructure

**Objective:** Establish the foundational enterprise environment.

- Deploy cloud infrastructure.
- Configure virtual networks and subnets.
- Deploy OPNsense.
- Implement routing and firewall policies.
- Configure WireGuard remote access.
- Deploy Active Directory and DNS.
- Configure shared enterprise services.
- Establish initial backup procedures.

**Expected Deliverable:** A functional enterprise environment with controlled network connectivity.

### Month 2 — Cybersecurity Monitoring

**Objective:** Implement centralised threat detection and security monitoring.

- Deploy Wazuh.
- Configure Windows Sysmon.
- Deploy Suricata.
- Integrate firewall and endpoint logs.
- Develop custom detection rules.
- Deploy secure and vulnerable web applications in their respective security zones.
- Establish incident monitoring workflows.
- Validate security event collection.

**Expected Deliverable:** A functional security monitoring environment capable of detecting selected simulated attacks.

### Month 3 — AI Integration and Evaluation

**Objective:** Integrate offensive and defensive AI capabilities.

- Develop the offensive AI controller.
- Implement approved attack simulations.
- Develop the defensive AI investigation pipeline.
- Integrate the Python policy engine.
- Implement limited autonomous responses.
- Test detection and containment.
- Evaluate performance and reliability.
- Finalise documentation and deployment automation.
- Validate backup, restoration, and project archiving procedures.

**Expected Deliverable:** An integrated AI-assisted cybersecurity environment with documented testing results.

---

## 10. Testing and Evaluation

MineNet will evaluate the effectiveness of its security architecture through controlled experiments.

### Evaluation Areas

- Network connectivity and segmentation
- Firewall policy enforcement
- Authentication and access control
- Security event collection
- Threat detection accuracy
- AI-assisted alert investigation
- Autonomous response effectiveness
- False-positive handling
- Incident response time
- Backup and recovery
- Infrastructure restoration

Testing results will be documented using logs, configuration evidence, screenshots, and performance measurements.

---

## 11. Future Development

MineNet is designed as an expandable cybersecurity engineering project.

Potential future enhancements include:

- Additional enterprise departments
- Site-to-site WireGuard VPN
- Multi-site enterprise networking
- Microsoft Entra ID integration
- Advanced offensive AI capabilities
- Expanded defensive automation
- Threat intelligence enrichment
- Vulnerability management dashboards
- Compliance and risk management
- Multi-cloud infrastructure
- Additional security monitoring integrations

Future development will build upon the existing architecture rather than requiring the entire environment to be recreated.

---

## 12. Project Documentation

Documentation will be maintained throughout development.

Planned documentation includes:

- Network architecture diagrams
- Cloud deployment procedures
- Firewall and routing configurations
- Active Directory configuration
- Security monitoring deployment
- Detection engineering
- AI integration and response architecture
- Controlled attack testing
- Troubleshooting records
- Backup and recovery procedures
- Performance evaluation reports

Implementation evidence and completed deliverables will be added as development progresses.

---

## 13. Project Status

**Current Phase:** Planning and Architecture Design

MineNet Version 1.0 is currently in the planning stage.

The features and technologies described in this repository represent intended implementation objectives and may evolve during development.

Completed components, test results, and technical documentation will be published progressively.

---

## Disclaimer

MineNet is an independent educational cybersecurity project.

All offensive security activities are intended to operate exclusively against authorised, isolated laboratory infrastructure. The project will use synthetic enterprise data and implement safeguards to prevent unintended effects on external systems.

---

**MineNet — Enterprise Infrastructure | Cybersecurity Engineering | AI-Assisted Security Operations**
