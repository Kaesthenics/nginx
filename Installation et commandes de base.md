# NGINX

## Installation / Commande de base
```
sudo apt-install nginx
```

### Lister les processus nginx
```
ps aux | grep nginx
```

### Afficher son ip
```
ip addr
```

### Démarrer/Recharger/Eteindre nginx
```
systemctl start|stop|reload nginx
```

### Activer ou désactiver le démarrage nginx au démarrage du serveur
```
systemctl enable|disable nginx
```

### Connaitre le statut nginx
```
systemctl status nginx
```

### Vérifier le config nginx
```
sudo nginx -t
```
