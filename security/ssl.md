# SSL

## générer une clé et un cerfiticat SSL
```
sudo openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout /etc/ssl/self.key -out /etc/ssl/self.crt

```

## Répondre aux questions
Output
Country Name (2 letter code) [AU]:FR
State or Province Name (full name) [Some-State]: none
Locality Name (eg, city) []:none
Organization Name (eg, company) [Internet Widgits Pty Ltd]: none
Organizational Unit Name (eg, section) []: none
Common Name (e.g. server FQDN or YOUR name) []: none
Email Address []:none
 