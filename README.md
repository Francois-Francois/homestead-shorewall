# homestead-shorewall
Shorewall configuration files for better secure on your Forge droplet


## How to use it

Log in ssh to your VM and run : 

```console
sudo aptitude install shorewall
cd /etc/shorewall
git clone https://github.com/rikless/homestead-shorewall.git
cd homestead-shorewall
mv * ../ && cd ../
rm -rf homestead-shorewall README.md
```

And then test your configuration :

```console
shorewall check
```

and be sure to get this message : 
Shorewall configuration verified

If there is any issue, be sure to disable the possibility to start shorewall :

Edit the /etc/shorewall/shorewall.conf and set : 

```console
STARTUP_ENABLED=No
```

This is temporary, fix the problem, check shorewall configuration again, and get back to Yes when you have : Shorewall configuration verified.

## Start your firewall

Now that all is ok, you can run :

```console
/etc/init.d/shorewall start
```







