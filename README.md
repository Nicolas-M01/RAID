# RAID
---

Il existe différends types de raid.  
### RAID 0  
la configuration RAID 0 permet d'améliorer la performance du système en répartissant 50% des données sur un disque et 50% sur l'autre.
Les deux disques travaillant simultanément, on dispose ainsi de performances deux fois plus élevée.
Soit une donnée A et une donnée B :  

• Volumétrie utile = Volumétrie totale
Les données n'étant pas dupliquées, il n'y aura pas de perte de volume stokage.

• Sécurité des données : FAIBLE
Il est fortement déconseillé d'utiliser cette configuration pour des serveurs assurant les services critiques de votre entreprise. Les données n'étant à aucuns moments dupliquées seront perdues si un des deux disques venait à être défectueux.

• Fonctionne uniquement sur deux disques
Il permet :  
* Un gain de performance.  
* D'avoir autant d'espace de stockage que la somme des disques utilisés.  
  ![image](https://github.com/user-attachments/assets/69869bd7-caa3-450e-97c4-35c5b465ac99)
---
  
### RAID 1  
La configuration RAID 1 permet de sécuriser un système en disposant de deux disques avec exactement les mêmes données. Dans cette configuration on ne recherche pas la performance mais plutôt la sécurité.  
Soit une donnée A et une donnée B :  

• Volumétrie utile = Volumétrie totale / 2  
Le disque 1 contenant exactement les mêmes données que le disque 2, la volumétrie utile sera divisée par 2.  

• Sécurité des données : BONNE  
Si un disque venait à être défaillant, cela ne poserait pas de problèmes car le second prendrait directement le relais.  
Il permet :  
* De la tolérence de panne  
![image](https://github.com/user-attachments/assets/931f7667-c8e2-4ba7-8199-83a3b8f798ed)
---

### RAID 5  
La configuration RAID 5, par un système de parité, répartit une petite partie des données sur chaque disque.  
Dans cette configuration, ce n'est pas la performance qu'on recherche mais plutôt la sécurité tout en économisant le volume de stockage.  
Soit une donnée A, une donnée B et une donnée C :  

• Volumétrie utile = Nombre de disques - 1 X capacité d'un disque  
Pour 3 disques de 200 Go, on aurait ainsi 3 -1 X 200 = 400 Go de volumétrie utile.  

• Sécurité des données : CORRECTE  
Dans cette configuration, on ne peut se permettre de perdre qu'un seul disque.  

• Nombre de disques nécessaires : Au moins 3  
Il permet :  
* Un gain de performance.  
* De la tolérence de panne.  
![image](https://github.com/user-attachments/assets/162267dc-34cc-4e5a-a5d8-91db82503808)

---
### RAID 10  
La configuration RAID 10 répartit dans une première grappe les données en RAID 0, et dans une seconde grappe temps en RAID 1.  
Celle-ci permet ainsi de disposer du niveau de sécurité de la configuration RAID 1 avec les performances qu'offre la configuration RAID 0.  
Soit une donnée A et une donnée B :  

• Volumétrie utile = Volumétrie totale / 2  

• Sécurité des données : BONNE  
Cette configuration offre un très bon niveau de sécurité car pour qu'une défaillance globale apparaisse, il faudrait que tous les éléments d'une grappe présentent un défaut en même temps.  

• Nombre de disques nécessaires : Au moins 4  

![image](https://github.com/user-attachments/assets/c092cd22-8991-40f8-847a-33d13623f48b)
---
