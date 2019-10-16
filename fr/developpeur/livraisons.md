---
title: Créer des livraisons à travers l'API
lang: fr
role: dev
ref: dev-api-deliveries
parent: Guide du développeur
nav_order: 2
---

# Créer des livraisons à travers l'API

En tant que client, vous souhaiterez probablement pouvoir créer des livraisons depuis un système externe.

Après avoir obtenu [vos identifiants API et vous être authentifié](/fr/developpeur/api.html), vous pouvez utiliser le point d'accès `/api/deliveries` pour créer des livraisons.

Les informations minimales dont nous avons besoin pour les points de retrait et de dépôt sont **l'adresse et l'horaire**.
Toutes les autes informations sont optionnelles.

## Créer une livraison avec les coordonnées géographiques

Si vous disposez des coordonnées géographiques précises des points à livrer, vous pouvez les fournir directement.
C'est la méthode préférée pour créer des livraisons.

```
{
    "pickup": {
        "address": {
            "streetAddress": "56, Rue de Dunkerque, Paris, France",
            "latLng": [48.882130, 2.347731]
        },
        "before": "2018-08-29 13:00:00"
    },
    "dropoff": {
        "address": {
            "streetAddress": "48, Rue de Rivoli, Paris France",
            "latLng": [48.857127, 2.354766]
        },
        "before": "2018-08-29 13:30:00"
    }
}
```

## Créer une livraison avec géocodage

S'il ne vous est pas possible d'obtenir les informations géographiques des points de retrait et de depôt, il est possible de fournir l'adresse sous forme de texte. Dans ce cas, l'adresse sera géocodée.

**Attention** : veillez cependant à fournir l'adresse la plus précise possible (au minimum, avec le nom de la ville)

```
{
    "pickup": {
        "address": "56, Rue de Dunkerque, Paris, France",
        "before": "tomorrow 13:00"
    },
    "dropoff": {
        "address": "48, Rue de Rivoli, Paris, France",
        "before": "tomorrow 13:30"
    }
}
```

## Créer une livraison avec une adresse de retrait implicite

En général, une adresse de retrait par défaut est attribuée à votre compte utilisateur.
Si c'est le cas, il n'est pas nécessaire de spécifier l'adresse de retrait, vous pouvez spécifier seulement l'adresse de dépôt.


```
{
    "dropoff": {
        "address": "48, Rue de Rivoli, Paris, France",
        "before": "tomorrow 13:30"
    }
}
```

## Créer une livraison en précisant un créneau horaire

En général, les horaires de retrait et de dépôt sont spécifiés sur un créneau horaire plus ou moins large.
De votre côté, vous devez vous assurer que la personne qui doit remettre la marchandise ou la réceptionner sera disponible sur le créneau horaire choisi.

Dans les exemples précédents, nous avons utilisé la propriété `before` pour spécifier l'horaire limite, mais si vous disposez de l'information, vous pouvez également utiliser la propriété `after` pour spécifier le début du créneau.

```
{
    "dropoff": {
        "address": "48, Rue de Rivoli, Paris, France",
        "after": "tomorrow 12:30"
        "before": "tomorrow 13:30"
    }
}
```

Vous pouvez également utiliser la propriété `timeSlot` pour spécifier le créneau.
L'exemple ci-dessous est équivalent à l'exemple précédent.

```
{
    "dropoff": {
        "address": "48, Rue de Rivoli, Paris, France",
        "timeSlot": "2018-08-29 12:30-13:30"
    }
}
```

**Attention** : il est possible que dans un futur proche, les créneaux utilisables soient soumis à une validation.
Cela signifie que vous devrez vous accorder à l'avance avec la société de livraison sur les créneaux que vous pourrez utiliser.
