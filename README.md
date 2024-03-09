# Mini serveur web

## Principe

Ce projet consiste à la combinaison de deux entités : 

- un "mini serveur" multi-threadé, `sioux`, qui décode les requêtes HTTP qui lui sont transmises
- un système de capture de paquets réseau, `ablette`

`ablette` réalise les tâches suivantes :

- capture des paquets sur l'interface réseau passée en paramètre ;
- filtrage des paquets à destination de la machine locale et vers des ports passés en paramètre ;
- détermination du top 5 des sources envoyant le plus de paquets sur les ports ciblés ;
- présentation de ces statistiques à sioux sous la forme d'une mémoire partagée.

## Utilisation

### Sioux

Pour utiliser `sioux`, il faut taper dans le dossier sioux:

```bash
sudo ./serveur -p <port>
```

### Ablette

Pour utiliser `ablette`, il faut taper dans le dossier ablette :

```bash
sudo ./ablette -i <interface> -p <ports>
```
Si plusieurs ports sont spécifiés, ils doivent être séparés par des virgules et sans espace.
Exemple: -p 443,80,8000




