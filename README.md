# homestead-shorewall
[Laravel Homestead](http://laravel.com/docs/5.0/homestead) comes with different applications to save time on site deployment. But, you can deploy quickly, and get a secured application on [Forge](https://forge.laravel.com/)

Shorewall is a gateway/firewall configuration tool for GNU/Linux.
For a high level description of Shorewall, see the Introduction to Shorewall. To review Shorewall functionality, see the [Features Page](http://shorewall.net/shorewall_features.htm).

## How to use it

Log in ssh to your VM and run : 

```console
sudo aptitude install shorewall
sudo cd /etc/shorewall
sudo git clone https://github.com/rikless/homestead-shorewall.git
sudo cd homestead-shorewall
sudo mv * ../ && cd ../
sudo rm -rf homestead-shorewall README.md
```

And then test your configuration :

```console
sudo shorewall check
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
sudo /etc/init.d/shorewall start
```







