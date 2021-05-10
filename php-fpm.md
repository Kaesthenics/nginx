# install

```
apt-get install php-fpm
```

# Vérif install

```
systemctl list-units | grep php
```

# Verif status

```
systemctl status php7.3-fpm.service
```

# Indiquer le chemin ou php socket est

```
sudo find / -name *fpm.sock
```

# Indique l'utilisateur propriétaire du processus de travail NGINX

```
ps aux | grep nginx
ps aux | grep php ->pour php
```

# Lister les paramètres les plus communs de fastcgi

```
cat /etc/nginx/fastcgi_params
```

```
user www-data;

events {

}

# Bloc d'exemple
http {

      include /etc/nginx/mime.types;

      server {

          listen 80;
          server_name nginx-handbook.test;
          root /srv/nginx-handbook-projects/php-demo;

          index index.php;

          location / {
              try_files $uri $uri/ =404;
          }

          location ~ \.php$ {
              fastcgi_pass unix:/var/run/php/php7.4-fpm.sock;
              fastcgi_param SCRIPT_FILENAME $realpath_root$fastcgi_script_name;
              include /etc/nginx/fastcgi_params; 
      }
   }
}
```
