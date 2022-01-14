# Apstra 4.0 - API Topology Configuration


EVE-NG topology and Apstra API Script to configure the DC automatically

Refer to this link to know more about the topology and eve-ng configuration for this project:

https://github.com/gilbertorgit/ent_sonic_apstra

## Authors

**Gilberto Rampini**

## Getting Started

### Pre-deployment Server Configs and Basic Packages

**Python Packages Installation**

```
lab@lab:~$ sudo su -

root@lab:~$ cd /home/lab

root@lab:/home/lab# add-apt-repository ppa:deadsnakes/ppa

root@lab:/home/lab# apt-get -y update

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

## EVE-NG Topology - Virtual Enterprise Sonic and Apstra - 3 Stage Clos DC

### Logical Topology
![Topology](https://github.com/gilbertorgit/ent_sonic_apstra/blob/main/sonic_3clos/topology_prints/Topology.png)

### EVE-NG Topology
![Topology](https://github.com/gilbertorgit/sonic-3-stage-clos-api/blob/main/eve-ng-topology.JPG)

