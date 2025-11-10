# Lab: Backend Automation with Ansible

## Demo   

This demo sets up a simple Flask web application on an Apache Web Server, backed by a MySQL database, using Ansible.

### Installation  

1. Create a docker container based off Ubuntu  

> port=$((10000 + RANDOM % 55535))  
> echo $port # Make sure the random number is between 10000 and 65535  
> docker run -v $PWD:/lab -w /lab -p $port:80 -it ubuntu bash  

2. Install Ansible  

> apt update  
> apt install -y ansible  

3. Install Git  
> apt install -y git  

4. Install text editors  

> apt install -y nano vim  

6. Deploy database  

> ansible-playbook database.yml  

7. Deploy webserver  

> ansible-playbook webservers.yml  

8. Deploy control packages  

> ansible-playbook control.yml

9. Test connection and endpoints

> curl 127.0.0.1
> curl 127.0.0.1/db  

