Installation
```
sudo apt-get install apache2-utils
```

htpasswd -c /etc/nginx/.htpasswd username

{
    location / {
        # Basic auth 
        auth_basic "message";
        auth_basic_user_file /etc/nginx/.htpasswd; 
    }
}