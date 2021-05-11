```
apt-get install siege
```

envoyer 2 requêtes de 5 clients différents
siege -v -r 2 -c 5 https://kaesthenics.fr

## définition de burst
burst: The burst parameter defines how many requests a client can make in excess of the rate specified by the zone
c'est une file d'attente après avoir dépassé les limites

http {

    limit_req_zone $binary_remote_addr zone=mylimit:10m rate=10r/s;
    
    location / {
        limit_req zone=mylimit burst=20 nodelay;
    }
}