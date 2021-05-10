# Dhparam

Générer une fichier dhparam
```
openssl dhparam 2048 -out /etc/nginx/ssl/dhparam.pem
```

Et ajouter cette ligne 

# Enable DH Params
ssl_dhparam /etc/nginx/ssl/dhparam.pem;