---
title: Refresh ✅
description: Route pour refresh un access token.
---

Route pour refresh un access token.

* **URL**

  /api/auth/access_token

* **Méthode:**
  
  `GET`

* **Paramètres:**

* **Cookie:**

  **Requis:**
  refresh_token
 

* **Réponse de succès:**

    * **Code:** 200 OK <br />
        **Contenu:** <br>
        ```json
        {
            "access_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VyIjp7ImlkIjo1LCJyb2xlIjoiVVNFUiJ9LCJpYXQiOjE3MDcyNDE0MTAsImV4cCI6MTcwODQ1MTAxMH0.S_NBFrkQpOzS6XNitdopFXca0gTweygpVdfMx8fPixk"
        }
        ```

* **Réponse d'erreur:**

    * **Code:** 400 Bad Request <br />
        **Contenu:**<br>
        `string => Invalid token`

    * **Code:** 400 Bad Request <br />
        **Contenu:**<br>
        `string => Token has expired. Please log in again.`
    
    * **Code:** 401 Unauthorized <br />
        **Contenu:**<br>
        `string => Unauthorized`

    * **Code:** 401 Unauthorized <br />
        **Contenu:**<br>
        `string => Access Denied. No token provided.`

    * **Code:** 500 Internal Server Error <br />
        **Contenu:**<br>
        `string => Internal Server Error`