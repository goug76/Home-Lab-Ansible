# 🏠 Goug's HomeLab Ansible Repository

**Description:**
This repository contains Ansible playbooks and related files designed to automate various aspects of a home lab environment, including tasks like automatic updates and new device provisioning.

---

## 📂 Repository Structure


```text
.
├── playbooks/
│   └── example_playbook.yml
├── LICENSE
├── README.md
└── test.yml
```


---
## ⚙️ Requirements
- Ansible 2.10 or higher​
- SSH access to target hosts​
- Ansible Vault or a similar secrets management tool for handling sensitive data

---

## 🔐 Secure Variables
This repository utilizes certain sensitive variables that should not be stored in the repository or exposed publicly. Ensure these variables are managed securely using Ansible Vault, environment variables, or your preferred secrets management solution.​

- Required Variables:
- admin_user: The administrative username for system access.​
- admin_password: The corresponding password for the admin_user.​
- smtp_server: SMTP server address for sending notifications.​
- webhook_url: (Optional) URL for webhook integrations to post results or logs.​

> Note: Never store sensitive values directly in this repository. Always utilize a secure method to manage these variables.

---

## 🚀 Usage
**Running a Playbook:**

To execute a playbook, use the following command:​

```bash
ansible-playbook -i inventory playbooks/example_playbook.yml --ask-vault-pass
```

1. Add the required secure variables at the project level within Semaphore.​
2. Configure a scheduled task as needed (e.g., every Saturday at 2 AM).​
3. Monitor execution results via webhooks or logs.

---

## 📝 License
This project is licensed under the MIT License. See the LICENSE file for details.

---

## 👨‍🔧 Maintainer
Goug's HomeLab
https://github.com/goug76

---