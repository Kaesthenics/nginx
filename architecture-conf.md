# Config server / virtual host

/etc/nginx/sites-available/
## 1- rajout d'une config server

exemple:
sudo touch /etc/nginx/sites-available/nginx-handbook

```
server {
    listen 80;
    server_name nginx-handbook.test;

    root /srv/nginx-handbook-projects/static-demo;
}
```

## 2- Rajout lien symbolique 
Now create a symbolic link to this file inside the /etc/nginx/sites-enabled/ directory by executing the following command:
sudo ln -s /etc/nginx/sites-available/nginx-handbook /etc/nginx/sites-enabled/nginx-handbook
ls -lh /etc/nginx/sites-enabled/ affichera le nouveau lien symbolique

