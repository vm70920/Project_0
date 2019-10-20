Using ansible playbook on EC2 AMI Linux:

Playbook designed to do: * install httpd server * edit httpd.conf file * copy index.html file into var/www/html folder * create group named Users * create 2 users * generate pair of ssh keys for each user * make users public keys authorized keys for access *restarts httpd
Clone repository into /tmp directory.

Before running ansible playbook:


	To check if ansible package is installed run:
  		$ ansible --version

	In case if ansible packege is not installed on host (for EC2 AMI Linux) run:
  		$ sudo pip install ansible

	After installation completed run:
		$ cd ansible
  		$ ansible-playbook setup_webserver.yml --check

	In case of successful validation run:
  		$ ansible-playbook setup_webserver.yml


