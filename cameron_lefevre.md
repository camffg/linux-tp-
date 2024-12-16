 # TP INSTALLATION NGINX et PROTECTION COMPLETE 

## Installation nginx

```bsh
sudo apt install nginx
```
### Configurer un pare-feu

```
sudo apt-get update

sudo apt-get install ufw

 sudo ufw default deny incoming
 
 sudo ufw default allow outgoing
 
 sudo ufw allow ssh
 ````

### Changer le port par défaut
````
  sudo ufw allow 2222/tcp
  
  sudo nano /etc/ssh/sshd_config
  
  sudo ufw enable
  
  sudo ufw status numbered

  sudo ufw reload
````

### Je créer un nouvel utilisateur

````
sudo sudo adduser defaultuser
````

````
 % ssh-keygen -t ed25519 -C "cameron.lefevre@gmail.com"

  ssh-copy-id -p 6218 defaultuser@wilfart.fr 
 `````

### Mise en place fail2ban
```bsh
sudo dnf install fail2ban

sudo apt install fail2ban -y

`/etc/fail2ban/jail.local`

 sudo apt install rsyslog

 sudo systemctl enable fail2ban

 sudo systemctl start fail2ban

```

Òs