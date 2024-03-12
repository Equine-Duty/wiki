---
title: Modifie un password  ✅
description: Route pour changer le mot de passe des users qui viennent de changer de role (Secretaire ou Organisateur) par email et change leur validation email pour true
---

Route pour changer le mot de passe des users qui viennent de changer de role (Secretaire ou Organisateur) par email et change leur validation email pour true.

* **URL**

  /api/resetpassword

* **Méthode:**
  
  `PUT`

* **Paramètres:**

  Content-Type: application/x-www-form-urlencoded

  **Requis:**

    Content-Type: application/json

    `old_password=[string]`<br>
    `new_password=[string|min 5]`<br>
   
* **Réponse de succès:**
  
  * **Code:** 200 <br />
    **Contenu:** 
    
    ```json
    {
      "Password updated"
    }        
    ```

* **Réponse d'erreur:**

* **Code:** 403 FORBIDDEN <br />
    **Contenu:** 
    ```json
    { "error": "The user is already verified." }
    ```

 * **Code:** 400 FORBIDDEN <br />
    **Contenu:** 
    ```json
    { "error": "Passwords do not match" }
    ```

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
