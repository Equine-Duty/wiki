---
title: Modifier le nom, le numéro de téléphone et la date de naissance du user ✅
description: Route qu'un user peut utiliser pour modifier son nom, son numéro de téléphone et sa date de naissance.
---

Route qu'un user peut utiliser pour modifier son nom, son numéro de téléphone et sa date de naissance.

* **URL**

  /api/users/{userId}/profile

* **Méthode:**
  
  `PUT`

* **Paramètres:**

  Content-Type: application/json

  **Requis:**
 
    `name=[string]`<br>
    `birthdate=[string]`<br>
    `phone=[string]`<br>

* **Réponse de succès:**
  
  * **Code:** 200 <br />
    **Contenu:** 
    ```json
    {
      "name": "Bob",
      "phone": "450-869-9045",
      "birthdate": "1992-07-03",
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
