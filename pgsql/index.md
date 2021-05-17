# Postgre

## Générale

Savoir si postgre est installé
```
pg_isready
```

Status de postgre
```
systemctl status postgresql
```

Créer un mot de passe pour l'utilisateur pgsql
```
sudo passwd postgres
```

Modifier le mot de passe du role postgres
psql -c "ALTER USER postgres WITH PASSWORD 'securepass_here';"

Démarrer terminal psql
```
psql
```

Créer un nouvel utilisateur
CREATE USER pg_mika PASSWORD ‘securep@ss_here’;     #assumes login function by default


## Commande utiles

### Start, restart, stop pgsql
systemctl start postgresql
systemctl restart postgresql
systemctl stop postgresql
systemctl reload postgresql


### Afficher les databases
\l+

### Afficher les users
\du
