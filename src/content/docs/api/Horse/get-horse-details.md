---
title: Recevoir les détails d'un cheval ✅
description: Route pour recevoir les détails d'un cheval.
---

Route pour recevoir les détails d'un cheval.

- **URL**

  /api/users/{userId}/horses/{horseId}

- **Méthode:**

  `GET`

- **Réponse de succès:**

  - **Code:** 200 <br />
    **Contenu:**
    ```json
    {
      "horse": {
        "id": 1,
        "name": "Thunder",
        "sex": "Male",
        "no_fei": "FEI123",
        "path_vaccine": "rd.pdf",
        "path_coggins": "rd.pdf",
        "user_id": 1
      },
      "owner": {
        "name": "Bob",
        "no_fei": "FEI321",
        "email": "Bob@gmail.com",
        "phone": "132-456-1254"
      }
    },
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

  - **Code:** 404 NOT FOUND <br />
    **Contenu:**
    ```json
    { "message": "La ressource n’existe pas." }
    ```
