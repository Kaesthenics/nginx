user www-data;

worker_processes auto;

events {
worker_connections 1024;
}

http {

include mime.types;
By default, NGINX compresses HTML responses
gzip on;
gzip_comp_level 3; // Niveau de compression 3 ou 4 est dans la moyenne

<!-- Les types de mimes compressibles -->

gzip_types text/css text/javascript;
## Dans l'entête réponse 
add_header Vary Accept-Encoding; // Important pour la compression
## Dans l'entête de la requête
"Accept-Encoding: gzip"




server {

    listen 80;
    server_name 167.99.93.26;

    root /sites/demo;

    index index.php index.html;

    location / {
      try_files $uri $uri/ =404;
    }

    location ~\.php$ {
      # Pass php requests to the php-fpm service (fastcgi)
      include fastcgi.conf;
      fastcgi_pass unix:/run/php/php7.1-fpm.sock;
      fastcgi_param REQUEST_METHOD $request_method;
      fastcgi_param SCRIPT_FILENAME $realpath_root$fastcgi_script_name;
    }

    location ~* \.(css|js|jpg|png)$ {
      access_log off;
      add_header Cache-Control public;
      add_header Pragma public;
      add_header Vary Accept-Encoding; // Important pour la compression
      expires 1M;
    }

}
}
