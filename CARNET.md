# 📒 Mon carnet de bord

**Nom :** 

**Prénom :** 

**Adresse de mon site :** https://sham.pythonanywhere.com

> Modifiez ce fichier directement sur GitHub (icône crayon ✏️) pour répondre aux questions de chaque exercice.
> Écrivez avec vos propres mots : une réponse courte et juste vaut mieux qu'un long copier-coller ! 🙂

---

## 🟢 Exercice 1 — Mon premier déploiement

1. Où se trouve physiquement le code qui fabrique votre page : sur votre ordinateur, sur GitHub ou sur PythonAnywhere ?

   > _Ma réponse : Sur pythonAnywhere et sur github

2. Pourquoi votre voisin(e) peut-il voir votre site, alors que vous n'avez rien installé sur son ordinateur ?

   > _Ma réponse : Car le site est hébergé en ligne sur un serveur
---

## 🟢 Exercice 2 — Les URL et les routes

1. Dans l'URL `https://www.google.com/maps`, quel est le nom de domaine ? Quel est le chemin ?

   > _Ma réponse : Nom de domaine : [www.google.com](https://www.google.com) Chemin (path) : /maps

2. Que veut dire le message *Not Found* ? Qui l'a envoyé : votre navigateur ou le serveur ?

   > _Ma réponse : La page ou la ressource demandée n'existe pas ou n'a pas été trouvée sur le serveur. C'est le serveur qui renvoie cette réponse 

3. Que se passe-t-il si deux fonctions portent le même nom dans `flask_app.py` ? (Indice : essayez, puis lisez l'Error log.)

   > _Ma réponse : cela provoque généralement une erreur au démarrage (AssertionError) car les routes utilisent par défaut le nom de la fonction comme identifiant unique (endpoint), et Flask refuse les doublons. 

---

## 🔵 Exercice 3 — Le langage HTML

1. Quelle est la différence entre ce que le serveur **envoie** et ce que le navigateur **affiche** ?

   > _Ma réponse : Le serveur envoie du code brut (HTML, CSS, JavaScript, texte). Le navigateur affiche le résultat visuel après avoir interprété et mis en forme ce code. 

2. À quoi servent les balises `<h1>`, `<p>`, `<ul>` et `<li>` ?

   > _Ma réponse : <h1> : Crée un titre principal (le plus important de la page).
<p> : Crée un paragraphe de texte.
<ul> : Crée une liste à puces (non ordonnée).
<li> : Crée un élément (une ligne) à l'intérieur d'une liste (<ul> ou <ol>).

3. Pourquoi l'image s'affiche-t-elle alors qu'elle n'est pas sur votre serveur ?

   > _Ma réponse : Parce que le lien de l'image (src) utilise une URL absolue (qui pointe vers un autre site ou un hébergeur d'images externe). Le navigateur va donc chercher et télécharger l'image directement sur ce serveur distant. 

---

## 🔵 Exercice 4 — Les templates

1. Pourquoi est-ce une bonne idée de séparer le code Python et le HTML ? (Pensez à une équipe avec un développeur et un graphiste.)

   > _Ma réponse : Cela permet au développeur de gérer la logique en Python et au graphiste de travailler sur le design en même temps sans interférer. 

2. Les `{{ prenom }}` sont-ils remplacés par le serveur ou par le navigateur ? Comment l'avez-vous vérifié ?

   > _Ma réponse : Ils sont remplacés par le serveur, ce qu'on vérifie en affichant le code source où la variable est déjà remplacée par sa vraie valeur. 

---

## 🔵 Exercice 5 — Le CSS et les liens

1. Quelle est la différence de rôle entre le HTML et le CSS ?

   > _Ma réponse : Le HTML structure le contenu de la page, tandis que le CSS gère son design et sa mise en forme. 

2. Pour afficher votre page `/presentation`, combien de fichiers le navigateur doit-il télécharger ? (Vous pourrez le vérifier à l'exercice suivant !)

   > _Ma réponse : Le navigateur doit télécharger au moins deux fichiers : le fichier HTML et le fichier CSS associé. 

3. Pourquoi faut-il parfois faire **Ctrl + F5** pour voir les changements de CSS ?

   > _Ma réponse : Il faut faire Ctrl + F5 pour forcer le navigateur à vider son cache et à retélécharger le fichier CSS mis à jour au lieu d'utiliser sa version enregistrée. 

---

## 🟣 Exercice 6 — Espionner le navigateur

1. Que signifie HTTP ? Qui envoie la **requête** et qui envoie la **réponse** ?

   > _Ma réponse : HTTP signifie HyperText Transfer Protocol le navigateur envoie la requête et le serveur envoie la réponse. 

2. Combien de requêtes votre page `/presentation` a-t-elle déclenchées ? Lesquelles ?

   > _Ma réponse : Elle a déclenché au moins deux requêtes : une pour charger le fichier HTML et une pour la feuille de style CSS. 

3. Que signifie le code `200` ? Et le code `404` de la favicon ?

   > _Ma réponse : Le code 200 signifie un succès, tandis que le code 404 de la favicon indique que l'icône du site n'a pas été trouvée par le serveur. 

4. Pourquoi les modifications faites dans l'onglet Éléments ne sont-elles pas visibles par les autres visiteurs ?

   > _Ma réponse : Car ces modifications sont faites localement dans votre propre navigateur, sans modifier le fichier original hébergé sur le serveur. 

---

## 🟣 Exercice 7 — Envoyer des informations dans l'URL

1. Dans l'URL `https://www.youtube.com/results?search_query=chat`, quel est le nom du paramètre ? Quelle est sa valeur ?

   > _Ma réponse : Le nom du paramètre est search_query et sa valeur est chat.

2. Pourquoi le serveur plante-t-il avec `a=bonjour` ? Que faudrait-il faire pour l'éviter ?

   > _Ma réponse : Le serveur plante si la variable est convertie en entier (ex: int('bonjour')), ce qu'on évite en vérifiant le type des données avec un bloc try/except. 

3. Pourquoi est-il dangereux d'afficher **tel quel** ce que l'utilisateur envoie ?

   > _Ma réponse : C'est dangereux car l'utilisateur peut injecter du code malveillant (faille XSS ou injection SQL), qui sera exécuté par le navigateur ou la base de données. 

---

## 🟣 Exercice 8 — Les formulaires

1. Quelle est la différence visible entre GET et POST ?

   > _Ma réponse : GET affiche les données dans l'URL, tandis que POST les cache discrètement dans le corps (body) de la requête. 

2. Pour un formulaire de **recherche**, quelle méthode choisiriez-vous ? Et pour un formulaire de **connexion avec mot de passe** ? Pourquoi ?

   > _Ma réponse : GET pour la recherche (pour avoir une URL partageable et mise en cache) et POST pour la connexion (pour ne pas exposer le mot de passe dans l'URL). 

3. Les données envoyées en POST sont-elles vraiment « secrètes » ? (Pensez à ce que vous avez vu dans l'onglet Réseau.)

   > _Ma réponse : Non, elles ne sont pas vraiment secrètes car elles sont lisibles en clair dans l'onglet Réseau du navigateur (bien que HTTPS les protège pendant le transport). 

---

## 🔴 Exercice 9 — Les codes de statut

1. Quelle est la différence entre une erreur `4xx` et une erreur `5xx` ? Qui est « fautif » dans chaque cas ?

   > _Ma réponse : Une erreur 4xx indique un problème venant du client (la faute du visiteur), tandis qu'une erreur 5xx vient du serveur (la faute du site web). 

2. Comment fonctionne une redirection ? Qui fait la deuxième requête : le serveur ou le navigateur ?

   > _Ma réponse : Le serveur indique une nouvelle adresse, et c'est le navigateur qui fait automatiquement la deuxième requête vers celle-ci. 

3. Donnez un exemple de situation où un vrai site utilise une redirection.

   > _Ma réponse : Un site redirige un utilisateur non connecté vers la page de connexion lorsqu'il essaie d'accéder à son espace personnel. 

---

## 🔴 Exercice 10 — Ce que le serveur sait de vous

1. Citez trois informations que le serveur connaît sur vous, sans que vous ayez rien rempli.

   > _Ma réponse : Le serveur connaît votre adresse IP, le type de navigateur (User-Agent) et votre langue système (Accept-Language). 

2. À quoi peut servir l'en-tête `Accept-Language` pour un site comme Wikipédia ?

   > _Ma réponse : Il sert à afficher automatiquement le contenu dans la langue préférée de l'utilisateur. 

3. Dans l'Access log, retrouvez une requête qui a reçu un code `404`. Quelle page était demandée ?

   > _Ma réponse : La page demandée est celle qui génère l'erreur 404 dans les logs (souvent /favicon.ico ou une URL inexistante). 

4. Après cet exercice, que pensez-vous de la notion de « navigation anonyme » ?

   > _Ma réponse : Elle masque l'historique sur votre appareil, mais le serveur distant continue de voir votre adresse IP et vos requêtes. 

---

## 🔴 Exercice 11 — Le Web des machines : API et JSON

1. Quelle est la différence entre une page HTML et une réponse JSON ? À qui chacune est-elle destinée ?

   > _Ma réponse : HTML est destiné à l'affichage visuel pour l'humain, tandis que JSON transporte des données brutes pour être traitées par du code ou un script. 

2. Dans la page `/horloge`, quel code s'exécute sur le **serveur** et quel code s'exécute dans le **navigateur** ?

   > _Ma réponse : Python s'exécute sur le serveur pour fournir l'heure de base, et JavaScript s'exécute dans le navigateur pour actualiser l'affichage en temps réel. 

3. Citez une application de votre téléphone qui, selon vous, utilise une API. Quelles données échange-t-elle ?

   > _Ma réponse : Une application météo utilise une API pour échanger des données de température et de prévisions avec un serveur distant. 

---

## 🏁 Pour conclure

En quelques phrases, expliquez à un ami ce qui se passe entre le moment où il tape une adresse dans son navigateur et celui où la page s'affiche :

> _Ma réponse : Tu tapes une adresse. Ton navigateur va chercher le contenu sur le serveur distant. Le serveur lui renvoie du code, et le navigateur le traduit pour afficher la page sous tes yeux. 
