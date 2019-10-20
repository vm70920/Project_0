Using ansible playbook on EC2 AMI Linux:

Clone repository into users home directory.

Before running ansible playbook:


To check if ansible package is installed run:
  $ ansible --version

In case if ansible packege is not installed on host (for EC2 AMI Linux) run:
  $ sudo pip install ansible

After installation completed run:
  $ ansible-playbook setup_webserver.yml --check

In case of successful validation run:
  $ ansible-playbook setup_webserver.yml


