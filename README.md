# RAID
---
<details>
<summary>
<h2>
:arrow_forward: Les différents types de RAID.  
</h2>
</summary>
  
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
</details>



<details>
<summary><h2> :arrow_forward: RAID 0 sous Windows (striping)  
</h2>
</summary>
Dans `Disk Management`  
`New striped volume` sur un des disques choisis pour le RAID 0  
---  
 
![Capture d'écran 2024-12-09 143633](https://github.com/user-attachments/assets/1985024c-ff5e-44f9-b7c5-aa45f2813301)  
---

Choisir le 2ème disque de réplication  
![Capture d'écran 2024-12-09 143654](https://github.com/user-attachments/assets/abea8da8-90e3-4e69-98a2-ce7a66d82c1e)  
---

Attribuer une lettre de lecteur pour le RAID 0  
![Capture d'écran 2024-12-09 143712](https://github.com/user-attachments/assets/54cab969-c19d-457a-9db6-6b9cc29977d6)  
---

Nommer le RAID 0  
![Capture d'écran 2024-12-09 143734](https://github.com/user-attachments/assets/09d7342e-ac6d-4328-8853-bd7b7bd7ee1f)  
---

Notre RAID 0 est prêt :  
![Capture d'écran 2024-12-09 143858](https://github.com/user-attachments/assets/b85d5579-b155-4993-a378-9fe9108cc9cb)  
---
</details>

<details>
<summary><h2> :arrow_forward: RAID 1 sous Windows (mirroring & duplexing)  
</h2>
</summary>
Dans `Disk Management`  
`New mirror volume` sur un des disques choisis pour le RAID 1  
  
---
![Capture d'écran 2024-12-09 151653](https://github.com/user-attachments/assets/3cc289f7-b705-4699-9bdb-644e7be502f1)

---
:hash: ``Choix de New mirrored volume" sur un des disques``  
![Capture d'écran 2024-12-09 151746](https://github.com/user-attachments/assets/264e4a2f-f40f-444b-bb74-7b3c94e8e0dc)
---
:hash: ``Ajout du 2ème disque``
![Capture d'écran 2024-12-09 151741](https://github.com/user-attachments/assets/91fc3a76-9be6-4fef-804b-1762aedd596b)
---

![Capture d'écran 2024-12-09 151727](https://github.com/user-attachments/assets/22953e0e-8dd1-4325-b74b-cf5568c3771f)
---
![Capture d'écran 2024-12-09 151721](https://github.com/user-attachments/assets/b98307a0-20ab-4939-bd21-cd32e2d4ecf7)
---
Notre RAID 1 est prêt
![Capture d'écran 2024-12-09 151830](https://github.com/user-attachments/assets/58653693-47b0-4d95-9e0f-2241fcbe3632)
---
</details>

  


<details>
<summary><h2> :arrow_forward: RAID 5 sous Windows (striping with parity)  
  </h2>
</summary>

:hash: ``Choix du RAID 5 sur un des disques``  
---
![Capture d'écran 2024-12-09 144702](https://github.com/user-attachments/assets/00b56046-4dad-4bb7-b988-491bce3ba27c)  

:hash: ``Ajout des 2 autres disques``  
---
![Capture d'écran 2024-12-09 144833](https://github.com/user-attachments/assets/5e6437fc-d424-438a-87e2-1dd5f5f558ec)  
:hash: Attribution de la lettre de lecteur  
---
![Capture d'écran 2024-12-09 144849](https://github.com/user-attachments/assets/a3f21d86-ff0b-4bb6-9867-bf96869434ce)  

:hash: Nom du RAId 5  
---
![Capture d'écran 2024-12-09 144908](https://github.com/user-attachments/assets/5f6c0204-d324-419a-862d-6561fc6a03b3)  
:hash: Le RAID 5 est créé. Pour 3Go on a 2Go  
---
![Capture d'écran 2024-12-09 144925](https://github.com/user-attachments/assets/74b41509-f58a-4c8a-92b1-4a77163a7b6c)  

:hash: Notre RAID 5 est prêt  
---
![Capture d'écran 2024-12-09 145242](https://github.com/user-attachments/assets/a565fce9-79b6-4bd7-906b-be291467d083)
</details>

