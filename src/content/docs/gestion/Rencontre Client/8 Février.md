---
title: 8 Février
---

## Ordre du jour
- État du projet
- Présentation des applications
  - App client
  - App admin
- Présentation des horaires
- Présentation de profil alternatif
- Rétroaction
- Questions sur le projet
  - Client
  - Admin
  - API

## Démos

### Client

- Création cheval : Sexe sont plus variés que male/femelle. (Jument, Cheval Castré, etc). Éric va envoyer une liste anglais/français.
- Pour la liste de compétitions en mode mobile, omettre certaines infos pour que tout rentre. Mettre une icone pour l’état de la compétition (ou peut-être tout simplement ne pas le montrer), et enlever nombre de places restantes.
- Design avec tout les infos du profil sur une page : Accepté, pas besoin de la barre de navigation à gauche. Cartes wrappent en dessous idéalement, mais pas de carrousel. Mettre bouton ajout à côté du label cavalier/cheval. 

### Admin

- Mettre les langues dans les paramètres. 
- Mettre le même nom pour les status et les filtres.  
- Modifier les boutons des show status 
- Date tardive seulement la fin de l’inscription tardive. 
- Si besoin de code pour l’inscription, il faut un checkbox pour dire si le coach doit donner son FEI. 
- Ajouter des autres frais en plus de ceux disponibles 
- Un test pour une classe. 
- Coggins (true par défaut) 
- Pour les rings on peut présenter d’avance le nombre de rings et les rings qui y seront. 
- Pour le schedule :  
  - Pas plus de 9h sans compter les pauses etc... 
  - Tu peux t’arrêter en plein milieu d’une classe. 
  - Si le test 1 doit durer 3 min 50, si tu dépasses, éliminer. 
  - Il y a plusieurs rings qui concourent tous en simultanée. (Pour le schedule) 
  - Séparer en classe pour le schedule 
  - Temps dans le test. 
  - La barre tout le temps visible. 
  - Les listes sont meilleurs UX que les cards. 

## Questions

### Client
- Doit-on ajouter une page de contact ou laissons nous simplement une card qui permet d'envoyer un courriel?
  - Champ pour entrer informations de contact, et qui les envoie à Éric. 
- Devrait-on afficher les timezone pour l'heure des compétitions?
  - Heure d’arrivée à ton box. Pas besoin de préciser le fuseau horaire. L’heure de ou tu es présentement est celle qui sera affichée.  
- Est-ce qu'il y aura des heures pour le début et fin des compétitions?
  - Ça va être avec l’horaire.   
- Avons-nous besoin d'une page contact us pour que les organisateurs puissent vous contacter pour créer des compétitions ? Si oui, que mettons-nous à l'intérieur ?
  - ???
- Que devons-nous mettre dans la page des détails des compétitions ?
  - Adresse, stalles totales restantes, nom organisateur, classes/tests disponibles, logo, nb places, montants, dates début/fin, juges 
- Dois on voir les juges dans les details de show.
  - Oui

### Admin
- Pour les class, dans le feedback vous dite 'le test associé' à la class, n'y-a-t-il qu'un test relié à une class?
  - Un seul test associé  

### API
- Pourrait-on avoir plus de précision sur les bundles?
  - Ils te donnent un prix, le nom du bundle et ce que ça comprend (une description).  

- Est-ce que l’utilisateur connecté peut choisir le nb de chaque achat unitaire ou juste des quantités générales 
  - Choisi le nombre que t’as besoin. 

### Notes autres/commentaires/suggestions

- Soft delete, sauf qu’il faut qu’on puisse toujours voir les résultats associés à cet utilisateur/cheval dans les compétitions sans que le site casse. Seulement besoin de garder nom du rider, nom du cheval, et nom du propriétaire. Sinon quand un user est delete, ajoute le nom du rider, du cheval, et du propriétaire à une autre table de users delete. 
- Ordre de passage en ordre décroissant de niveau pour un même cheval 
- Transition quand un cavalier fini sa reprise pas de break, le cavalier qui fini sort, et un autre cavalier entre, fait un tour de ring, et commence sa reprise. Pas de temps à perdre. 

## Petit rappel
- Logo et font
  - Designer a pris une semaine de plus de vacances. 