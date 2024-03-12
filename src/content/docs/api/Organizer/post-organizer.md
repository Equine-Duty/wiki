---
title: Créer un organisateur ✅
description: Route pour créer un nouveau organisateur. Si le user n'existe pas le compte est créé avec les information dans le body. Si le user existe, modifie un user pour mettre son role organisateur. Après le message de validation, envoit un email à l'adresse email avec le mot de passe temporaire envoyer dans le body. Le message lui demande de changer de mot de passe.
---

Route pour créer un nouveau organisateur. Si le user n'existe pas le compte est créé avec les information dans le body. Si le user existe, modifie un user pour mettre son role organisateur. Après le message de validation, envoit un email à l'adresse email avec le mot de passe temporaire envoyer dans le body. Le message lui demande de changer de mot de passe.

* **URL**

  /api/organizers

* **Méthode:**
  
  `POST`

* **Paramètres:**

  Content-Type: application/x-www-form-urlencoded

  **Requis:**

    Content-Type: application/json

    `name=[string]`<br>
    `email=[string]`<br>
    `phone=[string]`<br>
    `remaining_shows=[integer]`<br>
   
* **Réponse de succès:**
  
  * **Code:** 201 <br />
    **Contenu:** 
    Si le user n'existe pas 
    ```json
    {
      "User created"
    }        
    ```
    **Code:** 200 <br />
    Si le user existe
    ```json
    {
      "User updated"
    }        
    ```

* **Réponse d'erreur:**

  * **Code:** 401 UNAUTHORIZED <br />
    **Contenu:** 
    ```json
    { "message": "Non authentifié." }
    ```

  * **Code:** 403 FORBIDDEN <br />
    **Contenu:** 
    ```json
    { "message": "Cette action n’est pas autorisée." }
    ```
