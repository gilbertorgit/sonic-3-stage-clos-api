# Apstra 4.0 - Sonic 3 Stage Clos - API Apstra Configuration only

## Authors

**Gilberto Rampini**

## Getting Started

### Pre-deployment Server Configs and Basic Packages

**Python Packages Installation**

```
lab@lab:~$ sudo su -

root@lab:~$ cd /home/lab

root@lab:/home/lab# apt -y install software-properties-common

root@lab:/home/lab# add-apt-repository --yes ppa:deadsnakes/ppa

root@lab:/home/lab# add-apt-repository --yes --update ppa:ansible/ansible

root@lab:/home/lab# apt -y update

root@lab:/home/lab# apt -y install ansible git

root@lab:/home/lab# git clone https://github.com/gilbertorgit/sonic-3-stage-clos-api.git

root@lab:/home/lab# ansible-playbook sonic-3-stage-clos-api/base-pkg-kvm/playbook.yml
```

### Configure your Apstra IP URL

**Edit urls_base_apstra.py and add your Apstra MGMT IP** 

```
apstra_url = 'https://192.168.0.180:443'
```

### API Configuration

```
root@lab:# cd sonic-3-stage-clos-api/api_config/
root@lab:# python3.7 create_config_apstra_api.py 
```