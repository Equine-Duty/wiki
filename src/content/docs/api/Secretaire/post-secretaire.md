---
title: Créer une secretaire ✅
description: Route pour créer une nouvelle secretaire si le user n'existe pas ou modifier un user pour mettre son role secretaire dans un show. Après le message de validation, envoit un email à l'adresse email envoyer dans le body. Le message lui demande de changer de mot de passe.
---

* **URL**

  /api/shows/{showId}/secretaries

* **Méthode:**
  
  `POST`

* **Paramètres:**

  Content-Type: application/json

  **Requis:**

    `name=[string]`<br>
    `email=[string]`<br>
    `phone=[string]`<br>
   
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
