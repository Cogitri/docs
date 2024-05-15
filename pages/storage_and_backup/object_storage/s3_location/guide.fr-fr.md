---
title: Object Storage - Endpoints et géo-disponibilité de l’Object Storage
updated: 2024-05-15
---

<style>
td:nth-of-type(2) {
  white-space:nowrap;
}
</style>

Nous avons conçu les classes de stockage S3 pour qu’elles soient **compatibles avec l’API S3**, considérée comme une référence sur le marché du stockage objet. Vous pouvez donc utiliser l'Object Storage avec la plupart des outils de gestion de données via les points de terminaison définis par région et non par classe de stockage.

## Object Storage S3

OVHcloud Object Storage S3 est accessible via un point de terminaison unique : `https://s3.<region>.io.cloud.ovh.net`. Ce point de terminaison unique peut traiter à la fois les classes de stockage Standard et High Performance. Toutes les opérations de l'API S3 sont prises en charge avec ce point de terminaison unique.

### Liste des régions disponibles

| Nom de la région | Région<br><b><i>À saisir en minuscules</i></b> | Protocole | Version de la signature |
| ----- | ----- | ----- | ----- |
| Gravelines | gra | HTTPS | 4 |
| Francfort | de | HTTPS | 4 |
| Beauharnois | bhs | HTTPS | 4 |
| Roubaix | rbx | HTTPS | 4 |
| Varsovie | waw | HTTPS | 4 |
| Londres | uk | HTTPS | 4 |

Le point de terminaison de bucket est une URL, par exemple `https://my-bucket.s3.gra.io.cloud.ovh.net` qui représente un point de terminaison de style hôte virtuel.

### Mapping des niveaux de stockage AWS S3 vers les niveaux de stockage OVHcloud

Le mapping des opérations **WRITE(PUT)** sur le point de terminaison **io** est le suivant :

<table>
    <tr>
        <th>AWS</th>
        <th>Mapping OVHcloud actuel</th>
        <th>Mapping OVHcloud cible (à partir du 17/06/2024)</th>
    </tr>
    <tr>
        <td>Express One Zone</td> 
        <td rowspan=9>Standard</td>
        <td>High Performance</td>
    </tr>
    <tr>
        <td>Standard</td>
        <td rowspan=8>Standard</td>
    </tr>
    <tr>
        <td>Par défaut *</td>
    </tr>
    <tr>
         <td>Standard IA</td>     
    </tr>
    <tr>
        <td>Intelligent Tiering</td>
    </tr>
    <tr>
        <td>One Zone IA</td>
    </tr>
    <tr>
        <td>Glacier Instant Retrieval</td>
    </tr>
    <tr>
        <td>Glacier Flexible</td>
    </tr>
    <tr>
        <td>Glacier Deep Archive</td>
    </tr>
</table>

*_la classe de stockage par défaut sur le point de terminaison **io** sera Standard, c'est-à-dire que si vous ne spécifiez pas de classe de stockage ou si vous spécifiez une classe de stockage autre que celles fournies par AWS, votre objet sera stocké dans notre niveau Standard._

Le mapping des opérations **READ(GET/LIST/HEAD)** sur le point de terminaison **io** est le suivant :

<table>
    <tr>
        <th>AWS</th>
        <th>Mapping OVHcloud cible (à partir du 17/06/2024)</th>
    </tr>
    <tr>
        <td>Express One Zone</td> 
        <td>High Performance</td>
    </tr>
    <tr>
        <td>Standard</td>
        <td>Standard</td>
    </tr>
</table>

![Schema 1](images/io-mapping.png)

> [!warning]
> - La classe de stockage ne sera plus définie au niveau de la création du bucket, mais au niveau de l'upload d'objets individuels.
> - Le point de terminaison **perf** sera maintenu à des fins de rétrocompatibilité uniquement, afin de permettre aux outils qui ne prennent pas en charge la récente classe de stockage Express_One_Zone d'AWS de continuer à fonctionner sur notre object storage. Nous vous encourageons donc fortement à migrer vers le point de terminaison **io** cible chaque fois que cela est possible.

### Rétrocompatibilité des points de terminaison

Bien que le point de terminaison **io** soit le point de terminaison préféré pour accéder au service OVHcloud Object Storage, le point de terminaison **historique** `https://s3.<region>.perf.cloud.ovh.net` sera toujours maintenu à des fins de rétrocompatibilité pour les outils et les applications qui ne prennent pas en charge la dernière classe de stockage AWS Express_One_Zone.

Le mapping des opérations **WRITE(PUT)** sur le point de terminaison **perf** est le suivant :

<table>
    <tr>
        <th>AWS</th>
        <th>Mapping OVHcloud actuel</th>
        <th>Mapping OVHcloud cible (à partir du 10/06/2024)</th>
    </tr>
    <tr>
        <td>Express One Zone</td> 
        <td rowspan=9>High Performance</td>
        <td rowspan=3>High Performance</td>
    </tr>
    <tr>
        <td>Standard</td>
    </tr>
    <tr>
        <td>Par défaut *</td>
    </tr>
    <tr>
         <td>Standard IA</td>
        <td rowspan=6>Standard</td>
    </tr>
    <tr>
        <td>Intelligent Tiering</td>
    </tr>
    <tr>
        <td>One Zone IA</td>
    </tr>
    <tr>
        <td>Glacier Instant Retrieval</td>
    </tr>
    <tr>
        <td>Glacier Flexible</td>
    </tr>
    <tr>
        <td>Glacier Deep Archive</td>
    </tr>
</table>

*_la classe de stockage par défaut sur le point de terminaison **io** sera High Performance, c'est-à-dire que si vous ne spécifiez pas de classe de stockage ou si vous spécifiez une classe de stockage autre que celles fournies par AWS, votre objet sera stocké dans notre niveau High Performance._

Le mapping des opérations **READ(GET/LIST/HEAD)** sur le point de terminaison **perf** est le suivant :

<table>
    <tr>
        <th>AWS</th>
        <th>Mapping OVHcloud cible (à partir du 10/06/2024)</th>
    </tr>
    <tr>
        <td>Standard</td> 
        <td>High Performance</td>
    </tr>
    <tr>
        <td>Standard IA</td>
        <td>Standard</td>
    </tr>
</table>

![Schema 2](images/perf-mapping.png)

## Object Storage Swift

| Solution de stockage | URL du point de terminaison | Région disponible<br><b><i>À saisir en minuscules</i></b> |
| ----- | ----- | ----- |
| Object Storage SWIFT - Standard - Legacy |`https://s3.<region>.cloud.ovh.net` | Strasbourg : sbg<br>Londres : uk<br>Francfort : de<br>Varsovie : waw<br>Beauharnois : bhs<br>Gravelines : gra |

## Aller plus loin

Si vous avez besoin d'une formation ou d'une assistance technique pour la mise en oeuvre de nos solutions, contactez votre commercial ou cliquez sur [ce lien](/links/professional-services) pour obtenir un devis et demander une analyse personnalisée de votre projet à nos experts de l’équipe Professional Services.

Échangez avec notre communauté d'utilisateurs sur <https://community.ovh.com>.
