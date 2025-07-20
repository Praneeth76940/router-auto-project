  🧠 Network Automation using Ansible, Git & Jenkins (CI/CD)
This project showcases a fully automated workflow for configuring multiple Cisco routers using Ansible, managing changes with Git, and orchestrating deployments via Jenkins pipelines within a simulated lab powered by GNS3 and Ubuntu.

📚 Project Overview
This setup emulates a production-grade automation pipeline:
- 🔄 Configuration of multiple routers via Ansible.
- 📦 Version-controlled configurations stored in Git.
- 🚀 Jenkins automatically deploys updates after a Git commit.
- 🔐 Secure, repeatable config with Ansible Playbooks & SSH keys.

🏗️ Lab Topology
Ubuntu (Ansible + Git + Jenkins)
      |
      └── SSH Access
            |
      ┌───────────────┐
      │ Cisco Routers │
      └───────────────┘
         ├─ 192.168.42.1
         ├─ 192.168.42.2
         └─ 192.168.42.3



🔧 Technologies Used
| Tool | Role | 
| Ubuntu | Control node (automation server) | 
| Ansible | Automation & configuration management | 
| Git | Version control for infrastructure files | 
| Jenkins | CI/CD automation for playbook execution | 
| GNS3 | Network simulation platform | 
| SSH | Secure login and configuration transport | 



📁 Directory Structure
network-automation-lab/
├── inventory/
│   └── routers.ini           # Ansible inventory file
├── playbooks/
│   └── config_push.yml       # Main playbook to push config
├── roles/
│   └── router_config/
│       ├── tasks/
│       │   └── main.yml      # Task definitions
│       └── templates/
│           └── base_config.j2 # Jinja2 configuration template
├── jenkins/
│   └── Jenkinsfile           # CI/CD pipeline config
├── logs/
│   └── output.log            # Execution logs
├── .gitignore
└── README.md



✅ Key Features
- ⚙️ One-click config deployment across multiple routers
- 🔐 SSH key-based secure access
- 🧩 Jinja2 templating for reusable configs
- 🔁 Jenkins auto-triggers on Git updates or manually
- 🕒 Version history maintained through Git

🚀 Getting Started
Step 1: Clone This Repository
git clone https://github.com/your-username/network-automation-lab.git
cd network-automation-lab


Step 2: Configure Ansible Inventory
# inventory/routers.ini
[routers]
192.168.42.1
192.168.42.2
192.168.42.3


Step 3: Generate & Copy SSH Keys
ssh-keygen -t rsa
ssh-copy-id admin@192.168.42.1
ssh-copy-id admin@192.168.42.2
ssh-copy-id admin@192.168.42.3


Step 4: Run Ansible Playbook
ansible-playbook -i inventory/routers.ini playbooks/config_push.yml


Step 5: Jenkins CI/CD Setup
- Install Jenkins, Git, and Ansible plugins.
- Create a Freestyle or Pipeline Jenkins job.
- Pull the repository from GitHub.
- Set up Jenkins to execute your playbook on each commit or at scheduled intervals.

🧪 Sample Commands
# Check router SSH connectivity
ansible -i inventory/routers.ini routers -m ping

# Execute playbook with debug output
ansible-playbook -i inventory/routers.ini playbooks/config_push.yml -vvv



📸 Placeholder Screenshots
Replace these with real examples for maximum impact:
- ✅ Successful playbook execution
- ✅ Jenkins build output
- ✅ Git commit showing change
- ✅ Router CLI showing updated config

🌱 Future Enhancements
- Add rollback functionality with Git tags
- Enable dynamic inventory via API
- Integrate monitoring tools (e.g., Nagios or Prometheus)
- Implement role-based access control for Jenkins jobs

Let me know if you'd like this exported in a different format, tailored for a job application, or enhanced with visuals. Always down to help showcase your brilliance!
🏗️ Lab Topology
Ubuntu (Ansible + Git + Jenkins)
      |
      └── SSH Access
            |
      ┌───────────────┐
      │ Cisco Routers │
      └───────────────┘
         ├─ 192.168.42.1
         ├─ 192.168.42.2
         └─ 192.168.42.3



🔧 Technologies Used
| Tool | Role | 
| Ubuntu | Control node (automation server) | 
| Ansible | Automation & configuration management | 
| Git | Version control for infrastructure files | 
| Jenkins | CI/CD automation for playbook execution | 
| GNS3 | Network simulation platform | 
| SSH | Secure login and configuration transport | 

Directory Structure
network-automation-lab/
├── inventory/
│   └── routers.ini           # Ansible inventory file
├── playbooks/
│   └── config_push.yml       # Main playbook to push config
├── roles/
│   └── router_config/
│       ├── tasks/
│       │   └── main.yml      # Task definitions
│       └── templates/
│           └── base_config.j2 # Jinja2 configuration template
├── jenkins/
│   └── Jenkinsfile           # CI/CD pipeline config
├── logs/
│   └── output.log            # Execution logs
├── .gitignore
└── README.md



✅ Key Features
- ⚙️ One-click config deployment across multiple routers
- 🔐 SSH key-based secure access
- 🧩 Jinja2 templating for reusable configs
- 🔁 Jenkins auto-triggers on Git updates or manu

- 📸 Placeholder Screenshots
- ✅ Successful playbook execution
- ✅ Jenkins build output
- ✅ Git commit showing change
- ✅ Router CLI showing updated config
- 🌱 Future Enhancements
- Add rollback functionality with Git tags
- Enable dynamic inventory via API
- Integrate monitoring tools (e.g., Nagios or Prometheus)
- Implement role-based access control for Jenkins jobs

🙋‍♂ Author
Praneeth Reddy – Network Engineer
🔗 GitHub | LinkedIn






