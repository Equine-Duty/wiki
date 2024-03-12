---
title: Modifier son mot de passe ✅
description: Route qu'un user peut utiliser pour modifier son mot de passe.
---

Route qu'un user peut utiliser pour modifier son mot de passe.

* **URL**

  /api/users/{userId}/password

* **Méthode:**
  
  `PUT`

* **Paramètres:**

  Content-Type: application/json

  **Requis:**
 
    `old_password=[string]`<br>
    `new_password=[string]`<br>

* **Réponse de succès:**
  
  * **Code:** 200 <br />
    **Contenu:** 
    ```json
    {
      "message": "Password updated."
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

  * **Code:** 404 NOT FOUND <br />
    **Contenu:** 
    ```json
    { "message": "La ressource n’existe pas." }
    ```
