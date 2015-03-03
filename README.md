# homestead-shorewall
Shorewall configuration files for better secure on your Forge droplet


## How to use it

Log in ssh to your VM and run : 

```
sudo aptitude install shorewall
cd /etc/shorewall
git clone https://github.com/rikless/homestead-shorewall.git

```

Edit the /etc/shorewall/shorewall.conf and set : 

```
STARTUP_ENABLED=0
```

This is temporary, we will get back to 1 when we will be sure all is ok.

