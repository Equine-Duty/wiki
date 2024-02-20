---
title: Recevoir la liste des inscriptions d'un user ⛔
description: Route pour recevoir la liste des inscriptions d'un user.
---

Route pour recevoir la liste des users avec ou sans filtre.

- **URL**

  /api/users/{userId}/inscriptions

- **Méthode:**
  
  `GET`

- **Réponse de succès:**
  
  - **Code:** 200 OK <br>
    **Contenu:**<br>
    ```json
    {
        "inscriptions": [
            {
                "id": 1,
                "invoiceId": "294yocds839yr",
                "show": {
                    "id": 1,
                    "name": "Regional Quebec",
                    "start_date": "2024-11-24T03:10:52.634Z",
                    "city": "Montreal",
                    "zip_code": "123 abc",
                },
                "horse_name": "Rudolph",
                "rider_name": "Arthur",
            },
            ...
        ],
    }
    ```

- **Réponse d'erreur:**

  - **Code:** 401 UNAUTHORIZED <br />
    **Contenu:** 
    ```json
    { "message": "Non authentifié." }
    ```

  - **Code:** 403 FORBIDDEN <br />
    **Contenu:** 
    ```json
    { "message": "Cette action n’est pas autorisée." }
    ```
