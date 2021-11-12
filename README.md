# Ansible
- Intro
- ssh
- setup ansible in ubuntu 
- vagrant 
- command
- playbooks
- when conditions
- managing file 
- templates
- handlers (Optional)
- roles (Optional)

---
เตรียมเครื่อง 
- ติดตั้ง vagrant 
- ติดตั้ง oracle virtualbox
- ติดตั้ง ubuntu wsl2 
---
SSH
---
Adhoc
```
ansible all -m ping
ansible -i hosts all -m ping -u vagrant --key-file /home/arsom/.ssh/ansible
ansible -i hosts -m shell -a 'free -m' all -u vagrant --key-file /home/arsom/.ssh/ansible
ansible -i hosts -m command -a 'hostnamectl' all -u vagrant --key-file /home/arsom/.ssh/ansible
ansible -i hosts -m command -a 'df -h' all -u vagrant --key-file /home/arsom/.ssh/ansible
ansible -i hosts all -m apt -a update_cache=true  --key-file /home/arsom/.ssh/ansible -u vagrant
ansible -i hosts all -m apt -a update_cache=true  --key-file /home/arsom/.ssh/ansible -u vagrant --become --ask-become-pass
ansible -i hosts all -m apt -a name=net-tools  --key-file /home/arsom/.ssh/ansible -u vagrant --become --ask-become-pass
```
--- 
Playbooks

---
