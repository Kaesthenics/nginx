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

Créer un log depuis warning
```
server {

        listen 80;
        server_name nginx-handbook.test;

    	error_log /var/log/error.log warn;

        return 200 "..." "...";
    }
```

Récupérer la dernière ligne de log

```
sudo tail -n 1 /var/log/nginx/error.log
```

Les différentes niveaux d'alerts
debug – Useful debugging information to help determine where the problem lies.
info – Informational messages that aren't necessary to read but may be good to know.
notice – Something normal happened that is worth noting.
warn – Something unexpected happened, however is not a cause for concern.
error – Something was unsuccessful.
crit – There are problems that need to be critically addressed.
alert – Prompt action is required.
emerg – The system is in an unusable state and requires immediate attention.
