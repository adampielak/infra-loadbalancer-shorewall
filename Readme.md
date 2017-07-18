# enable instance to use non bound interfaces

> this tell the kernel we'll be using IP's that are not defined in the interfaces file

```sh
sudo vim /etc/sysctl.conf
net.ipv4.ip_nonlocal_bind=1
```

> this tells the server to activate what we put in the sysctl.conf file without rebooting the server

```sh
sysctl -p
```

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

