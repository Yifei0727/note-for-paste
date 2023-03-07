# note-for-paste
Common commands(shell), codes, templates, configuration information what 0^0 may use



* upgrade software and others update to date

`ubuntu` `system-admin` `shell` `debian`

```shell
sudo apt update && sudo apt upgrade -y && sudo apt autoremove --purge -y && sudo apt autoclean -y
```

* update project modules version in one commond

`developer` `java` `maven` `pom`

```
mvn versions:set -DnewVersion=a.b.c.d
```

```
sudo bash -c "echo 'Acquire::http { Proxy \"http://x.x.x.x:p\"; };'"  > /etc/apt/apt.conf.d/30proxy
sudo bash -c "echo 'Acquire::https { Proxy \"http://x.x.x.x:p\"; };'"  >> /etc/apt/apt.conf.d/30proxy
```
apt-cacher default port P is `3142`

```
# sudo snap set system proxy.http='http://x.x.x.x:p'
# sudo snap set system proxy.https='http://x.x.x.x:p'
# sudo snap get system proxy
```
squid default port P is `3128`

* install address  or use netplay cli
`ubuntu` `system-admin` `shell` `debian`

```
vi /etc/netplan/00-installer-config.yaml 
```
then edit
```
# This is the network config written by 'subiquity'
network:
  ethernets:
    enpXXsXX:  
      addresses:
        - N.N.N.N/N
      gateway4: N.N.N.N
      nameservers:
        addresses:
          - N.N.N.N
```

* docker

`docker` 

run instance shell for debug etc.
```
docker exec -ti {docker-instance} bash
```

test docker vlan quickly
```
docker network create --driver macvlan --subnet 192.168.0.1/24 --gateway 192.168.0.1 -o parent={if-name} work
docker run --net work --ip 192.168.0.123 -it --name macvlan-test --rm alpine /bin/sh
```
