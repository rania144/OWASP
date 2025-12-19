**Description** : Exploitation d'une injection SQL simple sur le formulaire de recherche des membres.

**Étapes techniques** :

Se rendre sur la page http://localhost:8080/?page=membe?.

Saisir la charge utile (payload) 1 OR 1=1 dans le champ de recherche.

Le serveur interprète 1=1 comme toujours vrai, ce qui force l'affichage de l'intégralité de la base de données des membres.

<img width="1301" height="965" alt="image" src="https://github.com/user-attachments/assets/6d211782-fb0b-4494-ab23-802642a8a770" />. Elle montre le membre nommé "Flag GetThe".



