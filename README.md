# install shorewall

```sh
sudo apt-get update
sudo apt-get install shorewall6
sudo apt-get install ipset
```

## edit shorewall.conf to read and save ipsets from/to file

`SAVE_IPSETS=Yes`

## copy config files in /etc/shorewall

## load shorewall configuration

```
cd /etc/shorewall
shorewall try .
shorewall start (/restart)
```

