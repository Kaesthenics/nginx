# Redirection

### Exemple de redirection 

```
location /logo {
    return 307 /thumb.png;
}
```


### Exemple de réécriture d'url 
A condition que /foo existe
````
rewrite /rewrite/\w+ /foo
```