# RAID
---

Il existe différends types de raid.  
### RAID 0  
#### Utilisé pour améliorer la vitesse de transfert en fusionnant plusieurs disques en un seul volume. Ainsi, pour lire un fichier d’1mo sur 2 disques durs, il lira 500ko sur les deux disques.  
Il permet :  
* Un gain de performance.  
* D'avoir autant d'espace de stockage que la somme des disques utilisés.  
  
### RAID 1  
#### C'est une duplication des données sur tous les disques durs de la matrice RAID. Cette méthode est la plus sûre pour le stockage de données sensibles.  
Il permet :  
* De la tolérence de panne  

### RAID 5  
C'est le plus utilisé en entreprise. Il permet d’améliorer les taux de transfert tout en tolérant une panne sur un disque dur. Le contrôleur RAID va écrire les données de la même manière qu’un RAID 0 mais ajoutera une parité (parity) sur un volume. Cette parité effectuera une rotation sur tous les disques à une fréquence régulière (strip-size).
Il permet :  
* Un gain de performance.
* * De la tolérence de panne.  

### RAID 10  
La configuration RAID 10 répartit dans une première grappe les données en RAID 0, et dans une seconde grappe temps en RAID 1.
Celle-ci permet ainsi de disposer du niveau de sécurité de la configuration RAID 1 avec les performances qu'offre la configuration RAID 0.
Soit une donnée A et une donnée B :

• Volumétrie utile = Volumétrie totale / 2

• Sécurité des données : BONNE
Cette configuration offre un très bon niveau de sécurité car pour qu'une défaillance globale apparaisse, il faudrait que tous les éléments d'une grappe présentent un défaut en même temps.

• Nombre de disques nécessaires : Au moins 4  
![image](https://github.com/user-attachments/assets/c092cd22-8991-40f8-847a-33d13623f48b)
