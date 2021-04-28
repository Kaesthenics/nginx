### Afficher le nombre de CPU et configurer un travailleur par CPU
lscpu
worker_processes <nombreDeResultats>;

### Affiche la limite du nombre de fichiers ouverts
 ulimit -n

### Changement du pid
Chemin de base:
```
/var/run/nginx.pid to /var/run/new_nginx.pid
```
