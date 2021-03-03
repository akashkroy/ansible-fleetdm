# ansible-fleetdm
Ansible playbook for Fleetdm

# Install Dependencies 
Install dependencies for mysql installation first 
```
ansible-galaxy install geerlingguy.mysql
```
# Generate TLS Certificates
Generate TLS Certs for fleetdm.
For Test servers and development server only . Use CA Issued certs in Production.

Open your terminal in the ansible-fleetdm folder and type the following: 
```
openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout conf/tls/fleetdm.key -out conf/tls/fleetdm.crt
```

# Adding variables 
Add your own keys and variables in **vars/main.yml** 

# Add hosts 
Add ip addresses in hosts file 

# How to run this script
```
ansible-playbook -i hosts deploy-fleet.yml
