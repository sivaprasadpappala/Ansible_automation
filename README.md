# Ansible Automation

Welcome to the Ansible Automation repository! This project contains Jinja-based templates and playbooks designed to streamline infrastructure automation and configuration management.

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [Directory Structure](#directory-structure)
- [Configuration](#configuration)
- [Contributing](#contributing)
- [License](#license)

## 🎯 Overview

This repository provides a comprehensive suite of Ansible automation tools and Jinja templates for managing infrastructure, deploying applications, and handling configuration management tasks. It leverages Jinja2 templating to create dynamic, reusable, and maintainable automation workflows.

## ✨ Features

- **Jinja2 Template Support**: Dynamic configuration generation using Jinja templates
- **Modular Playbooks**: Organized and reusable Ansible playbooks
- **Infrastructure as Code**: Define and manage your infrastructure declaratively
- **Configuration Management**: Automated system configuration and updates
- **Template Customization**: Easy-to-customize templates for various environments
- **Best Practices**: Follows Ansible best practices and standards

## 📦 Prerequisites

Before using this repository, ensure you have the following installed:

- **Ansible** (v2.9 or higher)
- **Python** (v3.6 or higher)
- **Jinja2** (v2.11 or higher)
- Git (for cloning the repository)

### Installation

1. **Clone the Repository**
   ```bash
   git clone https://github.com/sivaprasadpappala/Ansible_automation.git
   cd Ansible_automation
   ```

2. **Install Ansible**
   ```bash
   pip install ansible
   ```

3. **Install Required Dependencies** (if applicable)
   ```bash
   pip install -r requirements.txt
   ```

## 🚀 Usage

### Basic Playbook Execution

Run an Ansible playbook:
```bash
ansible-playbook playbook.yml
```

### Using Jinja Templates

Jinja templates can be used for dynamic configuration:
```bash
ansible-playbook -e "var_name=value" playbook.yml
```

### Inventory Management

Define your hosts in the inventory file:
```bash
ansible-playbook -i inventory playbook.yml
```

### Checking Playbook Syntax

Validate your playbook before running:
```bash
ansible-playbook --syntax-check playbook.yml
```

### Dry Run

Test without making changes:
```bash
ansible-playbook -C playbook.yml
```

## 📁 Directory Structure

```
Ansible_automation/
├── README.md                 # This file
├── inventory/               # Inventory files for hosts
├── group_vars/              # Group variables
├── host_vars/               # Host-specific variables
├── roles/                   # Ansible roles
│   └── role_name/
│       ├── tasks/           # Role tasks
│       ├── handlers/        # Event handlers
│       ├── templates/       # Jinja2 templates
│       ├── files/           # Static files
│       └── vars/            # Role variables
├── playbooks/               # Main playbooks
├── templates/               # Global Jinja2 templates
└── group_vars/              # Group-level variables
```

## ⚙️ Configuration

Configuration can be managed through:

1. **Inventory Files**: Define hosts and groups in `inventory/`
2. **Variable Files**: Use YAML files in `group_vars/` and `host_vars/`
3. **Playbook Variables**: Define variables directly in playbooks
4. **Jinja Templates**: Use dynamic templates for configuration files

### Example Variable Usage

```yaml
# group_vars/webservers.yml
web_server_port: 8080
app_version: 1.0.0
```

### Example Jinja Template

```jinja2
# templates/config.j2
server {
    listen {{ web_server_port }};
    server_name {{ server_name }};
}
```

## 🤝 Contributing

Contributions are welcome! To contribute:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

---

## 📞 Support

For issues, questions, or suggestions:
- Create an issue in the [GitHub Issues](https://github.com/sivaprasadpappala/Ansible_automation/issues) page
- Contact the repository maintainer

## 🔗 Quick Links

- [Ansible Documentation](https://docs.ansible.com/)
- [Jinja2 Documentation](https://jinja.palletsprojects.com/)
- [Ansible Best Practices](https://docs.ansible.com/ansible/latest/user_guide/playbooks_best_practices.html)

---

**Happy Automating! 🚀**
