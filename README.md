# Project_0

Goal of the project to design simple website running on webserver (AWS EC2 instance).

Major task breakdown:
 1. Obtain domain name
 2. Setup AWS account
 3. Setup AWS Virtual Private Cloud
 4. Setup webserver on AWS EC2
 5. Setup Domain
 6. Generate TLS certificate
 7. Create Ansible playbook
 8. Compose documentation
 
Collaboration tools: 
  * gitHub
Communication tools:
  * Slack

Virtual Private Cloud infrastructure includes:
 * 3 private subnets
 * 3 public subnets
 * 1 inetrnet gateway
 * 1 load balancer
 * 1 EC2 instance
 * 1 routing table for each type of subnets (private and public)
 
Public subnets accepting requests from all IPs routing them to internet gateway. Security Group monitors only HTTPS and SSH connections are going through.

Webserver httpd is running on EC2 instance accepting only https connections. 
Instance accepting ssh connection from remote hosts.
Basic webpage displays group name and group members
Domain name was purchased from Namecheap domain registrar.
DNS management conducted via AWS Route53
Domain name for the website: www.computing.monster
Private subnets connected to public via NAT instance
Certificate was obtained via AWS Certificate Manager
Loadbalancer implemented to manage traffic to instances in different availabiltiy zones, as well as instances itself
SSH key was generated at instance intitial setup. Copy of public key was stored on remote mahcine for remote access to instance (running webserver).
Ansible palybook meant to install httpd server, edit config file, setup group and users, genrate ssh keys for users and copy them to host authorized_keys. Ansible playbook functioning on 90% (there is bug in sharing public keys)
