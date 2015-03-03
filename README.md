# homestead-shorewall
Shorewall configuration files for better secure on your Forge droplet


## How to use it

Log in ssh to your VM and run : 

```
sudo aptitude install shorewall
cd /etc/shorewall
git clone https://github.com/rikless/homestead-shorewall.git

```

Always from the command line : 

```
cd homestead-shorewall
mv * ../ && cd ../
rm -rf homestead-shorewall README.md
```

And then test your configuration :

```
shorewall check
```

and be sure to get this message : 
Shorewall configuration verified

If there is any issue, be sure to disable the possibility to start shorewall :

Edit the /etc/shorewall/shorewall.conf and set : 

```
STARTUP_ENABLED=No
```

This is temporary, fix the problem, check shorewall configuration again, and get back to Yes when you have : Shorewall configuration verified.

## Start your firewall

Now that all is ok, you can run :

```
/etc/init.d/shorewall start
```










