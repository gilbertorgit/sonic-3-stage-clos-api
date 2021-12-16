# Apstra 4.0 - API Topology Configuration

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

