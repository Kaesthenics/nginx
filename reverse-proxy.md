# Utilisation basique reverse proxy

## Pensez à ajouter dans host <ip-server> nginx.test

```
server {
        listen 80;
        server_name nginx.test;

        location / {
                proxy_pass "https://nginx.org/";
        }
    }
```
