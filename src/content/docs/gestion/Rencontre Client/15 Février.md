---
title:  15 Février
---

# Ordre du jour

## État du projet

## Présentation des applications
- App client
- App admin

## Rétroaction

## Questions sur le projet
- Admin
- API

## App Client

- **SVGs**: Intégration des images vectorielles.
- **Navbar**: Logo + texte ou juste texte, selon l'esthétique préférée.
- **Inscription**: Pas de date de naissance requise lors de l'inscription de compte; à placer dans le profil du rider. L'inscription est restreinte aux personnes de 18 ans et plus.
- **Factures dans le profil**: La pagination est recommandée pour gérer efficacement les factures. Un système de filtrage/triage est également important. Amélioration de l'interface de recherche (bouton de recherche ou délai après la saisie).
- **Détails des factures sur mobile**: Informations essentielles telles que le nom, la date de l'événement et le numéro de facture avec un lien vers les détails complets.
- **Brouillon pour l'inscription**: Possibilité de sauvegarder les inscriptions en cours.
- **Gestion des inscriptions**: Interface permettant de visualiser et de modifier les inscriptions. Un bouton de paiement doit apparaître après le règlement.
- **Détails de la compétition**: Les informations telles que les tarifs, les règlements et l'organisateur sont accessibles uniquement aux utilisateurs connectés. Les visiteurs voient des messages incitant à se connecter pour plus d'informations.
- **Confirmation des règlements**: Ajout d'une case à cocher pour confirmer la compréhension des règlements lors de l'inscription.

## App Admin

- **Gestion des horaires**: Ajustement du nombre maximal de participants. Possibilité de modifier les horaires sans perturber le planning global. Gestion des conflits d'emploi du temps pour les juges.
- **Affichage des rings**: Tous les rings sont affichés simultanément.

## API
- **Liste des épreuves offertes**: Clarification sur la terminologie (tests ou marques).
- **Inscriptions multiples**: Possibilité de s'inscrire à plus d'une classe.
- **Signification des lettres pour les juges**: Les lettres dictent la position du juge, mais ne sont pas pertinentes pour l'application.
- **Paiement via Stripe**: Fonctionnalité confirmée opérationnelle.

## Admin
- **Tri des épreuves par niveau**: Priorité aux participants avec 2 chevaux. Association des classes et des rings.
- **Gestion des temps de pause**: Paramétrage des temps entre les passages des chevaux et des cavaliers.
- **Ordre de priorité des épreuves**: Bronze < Argent < Or < Grand Prix.
- **Planning des rings**: À discuter.
