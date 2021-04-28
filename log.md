Chemin accès aux log
```
ls -la /var/log/nginx
```

Créer un repertoire de log pour une uri
```
location /uri {
    access_log /var/log/nginx/uri.access.log;
    return 200 'Welcome to uri';
}
```

Récupérer la dernière ligne de log
```
sudo tail -n 1 /var/log/nginx/error.log
```