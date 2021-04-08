# Location

Pour les uri il y a différents moyens de configurer ces dernières
Les voici dans l'ordre des priorités (le 1er renporte sur le 2ème etc ...)

## 1- Exact match
```
location = /uri {
    return 200 'Ma réponse';
}
```

## 2- Preferential prefix match
```
location ^~ /uri {
    return 200 'Ma réponse';
}
```

## 3 Regex match
### Toutes les urls qui commencent par test et on un chiffre de 0 à 9 par exemple.
```
location ~* /uri[0-9] {
    return 200 'Ma réponse';
}
```

## 4 Prefix match
### La route la plus simple qui est la plus faible dans l'ordre des priorités
```
location ~* /uri[0-9] {
    return 200 'Ma réponse';
}
```