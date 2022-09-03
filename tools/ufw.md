

```
sudo nano /etc/default/ufw
sudo ufw default deny incoming
sudo ufw default allow outgoing
sudo ufw app list
sudo ufw allow ssh
```

```
sudo ufw status numbered
sudo ufw delete <number>
```

```
sudo ufw status verbose
sudo ufw enable
sudo ufw disable
sudo ufw reload
sudo ufw reset
```

#### Links
* [How To Set Up a Firewall with UFW on Ubuntu](https://www.digitalocean.com/community/tutorials/how-to-set-up-a-firewall-with-ufw-on-ubuntu-20-04)
* [How to Configure Ubuntu Firewall with UFW](https://www.cherryservers.com/blog/how-to-configure-ubuntu-firewall-with-ufw)
* [The Biggest Linux Security Mistakes](https://www.youtube.com/watch?v=QxNsyrftJ8I)
