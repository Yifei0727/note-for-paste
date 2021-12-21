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
sudo echo 'Acquire::http { Proxy "http://X.X.X.X:P"; };' > /etc/apt/apt.conf.d/30proxy 
```
