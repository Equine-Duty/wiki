---
title:  22 Février
---

22 Février 

# Ordre du jour 

## État du projet 

- Présentation des applications 
- App client 
- App admin 
- Stripe 
- Rétroaction 
- Éléments restant 
- Questions sur le projet 
- Client 
- Admin 

## Commentaires sur les applications  

### Client 

- Lazy loading, si possible pour les pages 
- Dans facture, QualDiv peut-être enlevé. Pour voir la facture dans Stripe, est apparemment payant alors peut-être à éviter.  

### Admin 

- Tout est good pour le moment 
- Page de Raph est bien 

### Stripe 

- Tout est good pour le moment 
- Quand un paiement se fait dans Stripe, pas envoyer en BD, juste gérer sur Stripe. Alors historique dans Stripe. 

## Questions 

### Client 

Pour l’horaire, quel sont les éléments importants à afficher? 

- Noms des juges, très importants. Conditionnel pour les lignes à droite (Lignes avec les lettres en haut). En partant de la gauche, important jusqu’à la ligne test en l’incluant. Possible de prendre un peu de liberté pour l’affichage des noms de juge, rendre ca beau. Visibilité plus importante. 

Quel sont les éléments nécessaires à compter pour les bundles? (Hay, chipping, box et stall?) 

- Hay, chipping, box, stall, plus un texte pour écrire du texte de plus. 

C’est quoi QualDiv dans la facture ? 

- Pas important, on peut l’enlever 

### Admin 

A quoi correspondent les nombre sur le fichier Nombre de Reprise 

- Le nombre de personnes qui sont inscrites. 

Lien foxvillage? 

- À enlever 

Types de break pour l’horaire 

- Il faut que les trois types soient utilisables dans l’horaire. 

## Éléments restant 

### Client 

- Terminer l’inscription -> Priorité 2  
- Horaires -> À partir du moment que c’est en BD nous pouvons l’afficher, nous allons voir avec Max -> Priorité 1 
- Billing manque des correctifs -> Priorité 3 
- Résultat de classement -> Component pourrait être partagé avec le côté Admin -> Priorité 4 
- Bundle -> Good si il y a des choses qui manquent -> Priorité 5 
- Authentification avec google -> Pas grave -> Priorité 6 

### API 

- Horaire  
- Scores 
- Mode brouillon -> s’il y a quelque chose, à éliminer 
- Colonne paiement -> Juste le total paiement. 
- Si on est capable, il faudrait lui envoyer la facture pour ne pas avoir à retourner sur le site pour voir la facture. Juste préciser si le participant a payé. 

### Admin 

- L’envoie des scores aux organisations -> On ne s’occupe plus de ça 
- Horaires des juges -> PDF que tu autogénère et imprime, dans le pire des cas Éric le fera 
- Paiement -> Juste à faire le lien quand le profil est créé, déjà géré du côté API -> Ajouter une page de succès pour les paiements. 
- Création d’horaire -> Si c’est trop lourd, c’est déjà beau comme ca
- Facture : Pour les frais de l’application, il faut afficher qu’est ce qu’on fait des frais. -> Pas vraiment de facture de leur côté, généralement sur Stripe. 
- Bundle -> Si on a le temps 
- Modification et suppression de résultat -> Ne pas se casser la tête tout de suite pour ça. 
- Affichage des scores -> Vient du client  
- Liste des inscrits et de toutes les choses achetées. 
- La secrétaire peut voir la liste de tout le monde et valider. 
- Si quelqu’un se désiste il faut l’ôter de l’horaire, et tout replacer dans l’horaire en fonction du changement des heures. -> Pas nécessaire mais Éric va voir avec son organisatrice pour vérifier, peut-être mettre une ligne qui barre le rider qui s’est désisté. 
- Pour la création pour le fichier du nombre de reprises: (Number of tests needed) C’est les impressions, c’est le nombre de personnes. 
- Pas de lien d’instructions pour la section. 
- Il faut que les riders soient barrés tant qu’on a pas choisi le juge.