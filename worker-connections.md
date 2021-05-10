### Afficher le nombre de CPU

nproc
worker_processes auto;

### Affiche la limite du nombre de fichiers ouverts

ulimit -n 
>output 1024

events {
worker_connections 1024;
}

### Changement du pid

Chemin de base:

```
/var/run/nginx.pid to /var/run/new_nginx.pid
```
