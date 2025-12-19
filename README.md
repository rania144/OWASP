# Faille 4 : XSS Stockée (Guestbook)

## Description
Cette vulnérabilité de type **Stored Cross-Site Scripting (XSS)** a été identifiée sur la page du Livre d'Or (Guestbook). Elle survient lorsque l'application web stocke une entrée utilisateur non filtrée (le message du livre d'or) et l'affiche ensuite à tous les utilisateurs visitant la page.

## Étapes de l'exploitation
1. **Accès au formulaire** : Navigation vers la page "Guestbook" du site BornToSec.
2. **Injection du payload** : Saisie d'un nom quelconque et insertion d'un script malveillant dans le champ "Message" : `<script>alert(1)</script>`.
3. **Exécution** : Validation du formulaire en cliquant sur "SIGN GUESTBOOK".
4. **Résultat** : Le script est enregistré sur le serveur. À chaque chargement de la page, le navigateur exécute le script et affiche le flag de sécurité.

## Preuve 
<img width="1721" height="900" alt="image" src="https://github.com/user-attachments/assets/32f1c44d-24ce-488a-a67b-00e62ce0b656" />

*Le flag obtenu est : 0FBB54BBF7D099713CA4BE297E1BC7DA0173D8B3C21C1811B916A3A86652724E*.

