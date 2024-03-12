---
title: Login ✅
description: Route pour connecter un user.
---

Route pour connecter un user.

* **URL**

  /api/auth/login

* **Méthode:**
  
  `POST`

* **Paramètres:**

  Content-Type: application/json

  **Requis:**
 
    `email=[string]`<br>
    `password=[string]`<br>

* **Réponse de succès:**
  
  * **Code:** 200 OK<br />
    **Contenu:** 
    ```json
    {
        "access_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VyIjp7ImlkIjo1LCJyb2xlIjoiVVNFUiJ9LCJpYXQiOjE3MDcxNjExNjEsImV4cCI6MTcwNzE2MTQ2MX0.9gay3zyazAuAX9oTElPskRoNWPw7vum65I63u1MzsdU"
    }
    ```

* **Réponse d'erreur:**

  * **Code:** 401 UNAUTHORIZED <br />
    **Contenu:** <br>
    `string => Email or passsword is invalid`
