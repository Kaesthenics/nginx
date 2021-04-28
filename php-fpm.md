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