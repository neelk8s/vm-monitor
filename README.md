# VM Monitor with Ansible

Automated VM resource monitoring and email alerting using Ansible.

## What it does
- Monitors CPU, Memory and Disk usage on local/remote machines
- Sends alert email when any metric exceeds threshold
- Uses Gmail SMTP for notifications

## Project structure
vm-monitor/
├── inventory.ini        # target hosts
├── playbook.yml         # main monitoring logic
├── group_vars/all.yml   # thresholds + SMTP config (not in repo)
└── templates/
    └── alert_email.j2   # HTML email template

## How to run
ansible-playbook -i inventory.ini playbook.yml -v

## Tech used
- Ansible
- Gmail SMTP
- Jinja2 templates
