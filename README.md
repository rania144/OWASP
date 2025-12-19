## Faille : User-Agent and Referer

**Description :** Cette vulnérabilité permet d'accéder à une page restreinte en manipulant les en-têtes HTTP de la requête. Le serveur vérifie si le navigateur est celui de la "NSA" via le Referer et un agent spécifique.

**Étapes de l'exploitation :**
1. Utilisation de PowerShell pour forger une requête HTTP personnalisée.
2. Définition du User-Agent : `ft_bornToSec`.
3. Définition du Referer : `https://www.nsa.gov/`.
4. Exécution de la commande pour afficher le flag caché.

**Preuve :**
![Capture du terminal PowerShell](./image_71db2c.png)

**Flag obtenu :**
`f2a29020ef3132e01dd61df97fd33ec8d7fcd1388cc9601e7db691d17d4d6188`

<img width="1301" height="965" alt="image" src="https://github.com/user-attachments/assets/6d211782-fb0b-4494-ab23-802642a8a770" />. Elle montre le membre nommé "Flag GetThe".




