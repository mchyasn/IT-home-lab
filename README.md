🧠 The Ultimate Home IT Lab — From Noob to Ninja
🚀 Why I Built It
This is not just a learning environment — it’s my personal cyber range, DevOps lab, and production-grade simulation platform. It exists to:
    • Test ideas
    • Break things
    • Automate recovery
    • Simulate attacks
    • Respond to threats
    • Deploy apps
    • Build infrastructure
    • Validate security controls
It mirrors real-world enterprise complexity with domains, subnets, firewalls, logs, alerts, containers, and more. I built this lab to sharpen my skills in:
    • 🧩 Infrastructure & Networking
    • 🔐 Cybersecurity & Blue/Red Team Practices
    • 🖥️ Server & Endpoint Management
    • 🤖 Automation & Orchestration
    • ☁️ Hybrid Cloud Design

🖥️ Core Lab Infrastructure
💾 Hypervisor Environment
    • Proxmox VE Cluster (3 nodes) on bare metal
    • ZFS RAID1 with SSD Caching
    • High Availability (HA) enabled
    • Centralized backups with Proxmox Backup Server
🛠️ Virtualized Machines & Containers
Role
OS
Purpose
DC01
Windows Server 2022
Active Directory, DNS, GPO, DHCP
FS01
Windows Server
File server with DFS, Shadow Copies
MGMT
Windows 10
Admin workstation with RSAT, PowerShell ISE
LNX-WEB
Ubuntu 22.04
Apache + NGINX reverse proxy
LNX-DB
Debian
PostgreSQL & MariaDB clusters
KALI
Kali Linux
Pen testing, red team tools
PFSENSE
pfSense CE
Firewall, VLAN gateway, OpenVPN
SIEM
Ubuntu
Wazuh + ELK SIEM stack
GRAYLOG
Docker
Syslog/NXLog log collection
HONEYPOT
T-Pot or Cowrie
Attack detection simulation
VAULT
HashiCorp Vault
Secrets management

🌐 Network Design (Simulated Enterprise)
VLAN Layout
    • VLAN 10 – Admin Zone (AD/DC, MGMT)
    • VLAN 20 – Workstations
    • VLAN 30 – Servers (Web, DB, SIEM)
    • VLAN 40 – DMZ (Internet-exposed services)
    • VLAN 50 – Red Team / Threat Simulation
    • VLAN 99 – Management VLAN (out-of-band)
Firewall Rules (pfSense)
    • Strict east-west traffic segmentation
    • No lateral movement without explicit rules
    • Transparent proxy with Snort/Suricata inline detection

🧪 Pro Labs (Real-World Simulation)
🔐 Active Directory Attacks & Defense
    • MITRE ATT&CK simulations: Golden Ticket, Password Spraying, DCSync
    • Event forwarding to Wazuh for real-time detection
    • Custom PowerShell alerting to Slack via webhook
☁️ Hybrid Cloud Simulation
AWS (Free Tier):
    • VPC with public & private subnets
    • IPSec VPN tunnel from pfSense
    • EC2 Web server + RDS MySQL backend
Terraform IaC:
    • Automating S3, EC2, and networking deployment
    • CloudFront + WAF for basic protection
⚙️ Automated OS Deployment
    • PXE boot server with iPXE + unattended Linux/Windows installs
    • Kickstart & Preseed configurations
    • Ansible playbooks for post-install automation

🛡️ SIEM & Log Pipeline
    • Wazuh Manager + agents on all endpoints
    • NXLog / Winlogbeat for Windows Event forwarding
    • Suricata IDS logs piped into ELK + Grafana dashboards
    • Alerting via Telegram bot & Slack webhooks

🎯 Offensive Lab
    • Red team tools: Metasploit, Cobalt Strike, custom payloads
    • Safe environments for reverse shells, phishing, privilege escalation
    • Blue team triages & responds using full SIEM visibility

🔄 Automation & CI/CD Stack
Tool
Use Case
Ansible
Server hardening, role-based provisioning
GitLab CI/CD
Push → test → Docker build → deploy to K8s
Terraform
AWS + Proxmox provisioning
Jenkins
Build pipelines, test automation
Vault/Consul
Secrets management & service discovery

🔎 Monitoring & Alerting
    • Uptime Kuma — Website/service uptime dashboard
    • Grafana + Prometheus — Node monitoring + resource alerts
    • Zabbix — Agent-based health/service checks

🔬 Cool Extras
✅ Honeypots (SSH, HTTP, SMB) reporting to Wazuh
✅ Custom GPO Templates (USB lockdown, BitLocker, screen timeout)
✅ Sysinternals tools auto-run via login script
✅ Windows Autopilot simulation for MDM onboarding
✅ NGINX reverse proxy with SSL & failover via Certbot

📦 Backups & Disaster Recovery
🔁 Automated ZFS snapshots + Proxmox snapshots
📦 Full VM backups to Synology NAS
🧪 Monthly recovery drills from backup images

🔮 Next Phase / Future Plans
🧬 Implement Zero Trust architecture with Tailscale
☁️ Expand cloud infra with Azure & GCP
🎣 Simulate phishing with Gophish + payload tracking
🧱 Build a SOC dashboard with end-to-end incident tracking
⚔️ Red vs. Blue game days with real scoring
👁️‍🗨️ Deploy Security Onion 2 for full-packet capture & threat hunting

🧱 Build a SOC dashboard with full incident lifecycle tracking
⚔️ Red vs. Blue game days: attack/defend scenarios w/ scoring
👁️‍🗨️ Deploy Security Onion 2 for full-packet capture & advanced threat hunting

🎓 What This Lab Proves About Me
✅ I can build and secure a full-stack enterprise-grade IT environment from scratch
✅ I understand real-world risks and how to monitor, defend, and automate around them
✅ I don’t just run commands — I build systems, break them, and rebuild smarter
✅ I can scale: from scripting a local VM to deploying in the cloud
✅ I treat my home lab like a production network — because practice is preparation

💼 My Advanced IT Home Lab
🧾 Overview
This project documents my journey of building a cutting-edge IT Home Lab. The environment is designed to simulate and solve real-world IT problems, covering everything from system administration, networking, cybersecurity, cloud computing, and automation. I use enterprise-level tools, advanced networking configurations, and security practices to replicate what happens in professional IT infrastructures.

🖥️ Lab Setup
Host System:
    • Processor: AMD Ryzen 9 5900X (12 cores, 24 threads)
    • RAM: 64 GB DDR4 ECC RAM (Error Correcting Code for higher reliability)
    • Storage: 1TB NVMe SSD (primary) + 4TB RAID 1 HDD (secondary for VM storage & backups)
    • GPU: Nvidia RTX 3070 (optional, for GPU-intensive tasks or virtual GPU workloads)
    • Networking: 10 Gbps Ethernet with dual NICs (for higher throughput, VLANs, and network isolation)
Virtualization Tools:
    • Proxmox VE
    • VMware ESXi
    • Docker & Kubernetes
Operating Systems:
    • Windows Server 2022
    • Ubuntu 20.04 LTS
    • CentOS 8 / Rocky Linux 8
    • Kali Linux
    • pfSense
    • Docker Containers

📁 Basic Labs (Fundamentals)
🔧 Basic Windows Server Tasks
✅ Installed Windows Server 2022 VM
✅ Set up Active Directory Domain Services (AD DS)
✅ Configured DNS and DHCP
✅ Configured GPOs
✅ Set up DFS
👨‍💼 Advanced Active Directory
✅ Domain Trusts and Forests
✅ Group Policy Hardening
✅ Delegation of Control
🐧 Advanced Linux Sysadmin
✅ NFS and Samba
✅ LVM
✅ SELinux
✅ Automated updates with Ansible

🚀 Advanced Labs (Pro)
🔁 Automated Windows Backup & Restore
🛠️ In Progress: Windows Server Backup + Veeam
✅ Full restore from Veeam
💻 PowerShell Scripting
✅ Automated AD User Management
✅ Custom AD Reports
🧠 Security Auditing
✅ Sysinternals + PowerShell for log auditing
✅ Microsoft Security Compliance Toolkit
🛠️ GPO Deployment & Hardening
✅ Advanced Security Policies
✅ System Hardening with Defender, BitLocker, Firewall
📊 Log Management & SIEM
🛠️ In Progress: Wazuh SIEM
✅ Graylog Integration
✅ Real-time monitoring with dashboards

💡 Expert Labs (Next-Gen IT)
🌐 Web Server Deployment
✅ Apache + SSL (Let’s Encrypt)
✅ IIS for ASP.NET
✅ Load Balancing with HAProxy/Nginx
☁️ Cloud Integration
🛠️ In Progress: Hybrid Cloud (AWS + Proxmox)
    • VPC with public/private subnets
    • IPSec VPN Tunnel
✅ AWS EC2 + S3
📸 screenshots/expert/aws-cloud-setup.png
🔒 Penetration Testing with Kali
✅ Kali VM with Metasploit, Nmap, Wireshark, Burp Suite
✅ Internal scanning + exploitation
✅ Detection via Suricata, Fail2ban, Wazuh
📸 screenshots/expert/pen-test.png
🧑‍💻 CI/CD Pipeline
✅ Jenkins from GitHub to web server
✅ Docker & Kubernetes deployment with Helm
📸 screenshots/expert/cicd-pipeline.png
🛡️ Advanced Network Security
✅ pfSense firewall rules and VPN
✅ Site-to-Site VPN with remote server

🧰 Tools by Category
🛡️ Networking & Security
    • pfSense
    • WireGuard
    • OpenVPN
    • Suricata
    • Snort
📊 Log Management & SIEM
    • Wazuh
    • Graylog
    • Elastic Stack (ELK)
⚙️ CI/CD & DevOps
    • GitHub
    • Jenkins
    • Docker
    • Helm
    • Kubernetes
☁️ Cloud
    • AWS
    • Azure (for hybrid environments)
🔓 Penetration Testing
    • Kali Linux
    • Nmap
    • Metasploit
    • Wireshark
    • Burp Suite

📌 Future Enhancements
🔒 Zero Trust Architecture
    • Simulate Zero Trust environments using tools like Tailscale and BeyondCorp models
🧠 AI-Driven Security
    • Experiment with SOAR (Security Orchestration, Automation, and Response)
☁️ Multi-Cloud Lab
    • Extend lab across AWS, Azure, and GCP for multi-cloud experience
🧪 Incident Response Playbooks
    • Build out full blue-team incident response and recovery scenarios
⚙️ Automated VM Provisioning
    • Fully automate infrastructure builds using Terraform + Ansible workflows

🧠 Ultimate Home Lab Portfolio
From Beginner to Expert — Realistic, Detailed & Practical

🏁 Phase 1: Foundation Setup (Beginner Level)
✅ Operating Systems to Install (on VMs)
OS
Use Case
Notes
Windows 10 Pro
Standard desktop for management
Enable RDP, join domain
Windows 11 Pro
Modern desktop testing
TPM + Secure Boot via VM
Windows Server 2019/22
Server-side testing
AD, DNS, DHCP, GPOs
Linux Mint
Beginner-friendly Linux
GUI practice, basic CLI
Ubuntu Server
Server practice
No GUI, pure CLI admin
Kali Linux
Security & penetration testing
Nmap, Metasploit, Burp
Debian / Arch (opt.)
Advanced Linux skills
Manual package/config
pfSense
Router/firewall OS
VLANs, IDS/IPS, DHCP, VPN
OpenMediaVault / TrueNAS
NAS & storage testing
SMB/NFS shares, RAID

🔧 Phase 2: Post-Installation Configuration
✅ Core Setup per OS:
    • Create local user: mchyasn
    • Set static IP & hostname
    • Install Guest Additions / KVM tools
    • Enable SSH / RDP / Sudo
    • Configure DNS & gateway
    • Set up shared clipboard/folders

📦 Phase 3: Software Install & Environment Setup
✅ Windows
    • Sysinternals Suite
    • Notepad++, Wireshark, Putty
    • PowerShell 7
    • Git + VS Code
    • Chocolatey for package management
✅ Linux
    • UFW / iptables
    • NGINX / Apache
    • Fail2Ban + ClamAV
    • Neofetch, htop, netstat
    • Git + VS Code + tmux
✅ Cross-Platform Tools
    • VirtualBox/KVM guest additions
    • Docker & Portainer
    • Python 3 + Pip
    • SSH keys & config files

🧠 Phase 4: Intermediate Lab Projects
✅ Networking & Services
Project
Description
AD DS + DNS + DHCP
Fully configured domain mchyasn.local
Group Policy Lab
User lockout, software deploy, security hardening
Shared Folders
Linux ↔ Windows SMB share testing
Remote Desktop Gateway
RDP through HTTPS
Apache & NGINX Hosting
Static site + reverse proxy
FTP / SFTP Servers
File transfer lab
Firewall Rules
VLAN-based rules in pfSense
OpenVPN / WireGuard
VPN server hosted on pfSense
📸 Screenshots:
    • Group Policy Editor
    • Shared Folder Permissions
    • RDP Gateway Login

🔐 Phase 5: Security & Blue Team Skills
✅ Defensive Projects
    • Windows Event Viewer + Custom Event Logs
    • Sysmon + Winlogbeat → ELK / Graylog
    • Install & configure Wazuh
    • Enable BitLocker & LUKS full-disk encryption
    • AuditPol: Enable auditing
    • Harden Windows with LGPO tool
✅ Offensive Projects
    • Kali + Metasploit → Exploit Windows 10
    • Crack passwords with John / Hydra
    • SQLMap on test DB
    • BurpSuite → MITM practice
    • Create phishing email in Gophish
📸 Screenshots:
    • Sysmon logs in Graylog
    • Kali terminal running SQLMap
    • BurpSuite intercept window

💡 Phase 6: Expert-Level Automation & Integration
✅ Automation with PowerShell
    • Bulk AD User Creation
    • Log Archiving
    • AD Group Management

🧠 Phase 6: Expert-Level Automation & Integration (continued)
✅ Bash Scripts (Linux Automation)
    • Package Installers for multiple distros
    • Service Monitoring + Auto-Restart via systemd or shell loop
    • CRON Jobs:
        ◦ Log cleanups
        ◦ Auto backups
        ◦ Security scans
✅ Monitoring & Logging Stack
    • PRTG Network Monitor – Agentless network monitoring
    • Prometheus + Grafana – Custom dashboards for server metrics
    • ELK Stack – Elasticsearch + Logstash + Kibana
    • Wazuh + OSSEC – SIEM with agent-based security monitoring
    • Zabbix – SNMP, ICMP, agent-based full network monitoring
    • Portainer – Docker container monitoring via web GUI
    • Veeam + Timeshift – Backup & restore testing for Windows and Linux

🔗 Integration & Visualization
    • GitHub: Push configs/scripts via CLI
    • Dockerized Services:
        ◦ ELK Stack
        ◦ Portainer
        ◦ Nextcloud (self-hosted cloud storage)
    • Network Map: Generated with nmap + exported to draw.io

🧠 Advanced IT Home Lab Projects
Domain: mchyasn.local
This section showcases advanced simulations and tools deployed in my home lab to build real-world enterprise skills in cybersecurity, networking, and systems automation.

🔐 1. ELK Stack SIEM (Elastic + Logstash + Kibana)
Goal: Monitor system and network logs from Windows, Linux, and pfSense.
    • ✅ Winlogbeat forwarding from Windows Server
    • ✅ Syslog ingestion from Ubuntu and pfSense
    • ✅ Dashboards: Failed logins, SSH brute-force, firewall blocks

🌍 2. Multi-Site Active Directory Forest
Goal: Simulate an enterprise with multiple locations and domains.
    • ✅ Domains: mchyasn.local & remote.mchyasn.local
    • ✅ Trust relationship between forests
    • ✅ AD Sites & Services: Defined subnets + site links

🦠 3. Red Team Simulation with Caldera
Goal: Run emulated cyberattacks and monitor defense.
    • ✅ Caldera agent deployed
    • ✅ MITRE ATT&CK operation: Privilege escalation + lateral movement
    • ✅ SIEM alerts triggered and logged

🔄 4. Backup & Disaster Recovery
Goal: Full system restore testing with snapshot workflows
    • ✅ Daily backups with UrBackup
    • ✅ Successful VM restore after simulated failure
    • ✅ Pre/post ransomware snapshots for forensics

🌐 5. Reverse Proxy + SSL with NGINX
Goal: Secure hosting of multiple services
    • ✅ Hosted vault.mchyasn.local, wiki.mchyasn.local
    • ✅ Wildcard SSL certs via Let's Encrypt
    • ✅ Auto-renewal + HTTPS redirect

📦 6. Kubernetes Lab (K3s + Grafana)
Goal: Container orchestration and visualization
    • ✅ K3s cluster deployed on VMs
    • ✅ Helm charts used to deploy apps
    • ✅ Grafana dashboards for container metrics

🛡️ 7. IDS/IPS with Suricata
Goal: Detect network-level threats and send alerts
    • ✅ Suricata connected to pfSense LAN
    • ✅ Alerting for port scans, IP anomalies
    • ✅ Wazuh + Suricata integration in dashboard

⚙️ 8. Ansible Lab Automation
Goal: Infrastructure-as-Code for repeatable deployments
    • ✅ YAML playbooks to install, configure, and join systems to domain
    • ✅ User + Group creation across systems
    • ✅ Agentless push from Ansible control node

🧑‍💻 OS Deployment Example
🪟 Step 1: Windows 10 VM – Install Drivers and Basic Apps
✅ Installed Chocolatey via PowerShell
✅ Automated App Installation with PowerShell script:
    • Google Chrome
    • 7-Zip
    • Notepad++
    • Git
    • VLC Media Player
    • Sysinternals Suite
    • CPU-Z
    • HWMonitor
    • TreeSize Free
    • Rufus
    • WinDirStat
    • Wireshark

🧑‍💻 Step 2: Windows 10 VM – Create Local Users & Manage Accounts
✅ Opened Settings > Accounts > Family & other users
✅ Added local users:
    • testuser1 (Standard)
    • testadmin (Administrator)
✅ Switched between accounts to test
✅ Changed account types via Control Panel
✅ Set and removed passwords
✅ Verified access control and permissions

🧑‍💻 Step 3: Windows 10,11 VM – Common Troubleshooting Practice
✅ Network
    • Disabled/re-enabled adapter
    • Ran Network Troubleshooter
    • Used: ipconfig, ping, tracert
✅ Windows Update
    • Checked for updates manually
    • Reviewed update history
    • Paused and resumed updates
✅ Printers
    • Simulated printer install
    • Checked Print Spooler service
    • Removed and re-added printers

🛡️ Step 4: Promote Windows Server to Domain Controller & Create AD Domain
✅ A. Set Static IP Address
    • IP: 192.168.1.10
    • Subnet: 255.255.255.0
    • Gateway: 192.168.1.1
    • DNS: 127.0.0.1
✅ B. Rename Server
    • Renamed to WIN-SERVER
    • Rebooted
✅ C. Install AD DS Role
    • Added Active Directory Domain Services
    • Added DNS Server
✅ D. Promote to Domain Controller
    • New Forest: lab.local
    • Set DSRM password
    • Server restarted as Domain Controller

🌐 Step 6: Configure DHCP and DNS on Windows Server
✅ A. DHCP Setup
    • Installed DHCP Server via Server Manager
    • Created IPv4 Scope:
        ◦ Name: Lab DHCP Scope
        ◦ Range: 192.168.1.100 – 192.168.1.200
        ◦ Subnet Mask: 255.255.255.0
        ◦ Gateway: 192.168.1.1
        ◦ DNS: 192.168.1.10
    • Activated scope and verified dynamic IP assignment
✅ B. DNS Setup
    • Verified Forward Lookup Zone: lab.local
    • (Optional) Verified Reverse Lookup Zone
    • Ran nslookup lab.local to confirm name resolution

🐧 Step 7: Ubuntu/Xubuntu VM – Basic Linux Administration
✅ A. Basic Terminal Commands
    • Used: pwd, ls, cd, mkdir, touch, rm
✅ B. User and Group Management
    • Created user: testuser
    • Set password for testuser
    • Created group: testgroup
    • Added testuser to testgroup
    • Deleted testuser after testing
✅ C. File Permissions and Ownership
    • Directory: /home/testfiles
    • File: myfile.txt
    • Ownership: chown testuser:testgroup myfile.txt
    • Permissions: chmod 755 and chmod 700
    • Verified with ls -l
✅ D. Software Management with APT
    • sudo apt update && sudo apt upgrade
    • Installed: htop
    • Removed: sudo apt remove htop

🌐 Step 8: Networking Between VMs
✅ A. Ping Between Machines
    • Checked IPs with ipconfig (Windows) / ip a or ifconfig (Linux)
    • Pinged each VM to verify connectivity
    • Verified ICMP replies across all VMs
✅ B. Shared Folder Over Network
    • Shared folder on Windows 10 VM
    • Enabled Network Discovery & File Sharing
    • Accessed using: \\<Windows_VM_IP>\SharedFolder
✅ C. Verified IP Configuration
    • Checked:
        ◦ IP Address
        ◦ Subnet Mask
        ◦ Default Gateway
        ◦ DNS Server
✅ D. DNS Resolution
    • Ran: nslookup lab.local and ping lab.local
    • Confirmed resolution to Domain Controller IP

✅ The lab network is fully functional and integrated across Windows and Linux VMs.
