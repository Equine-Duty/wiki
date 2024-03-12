---
title: Get des bundles ✅
description: Route pour get les bundle d'un show
---

Route pour get les bundle d'un show.

- **URL**

  /api/shows/{showId}/bundles

- **Méthode:**

  `POST`

- **Paramètres:**

  Content-Type: application/x-www-form-urlencoded

- **Réponse de succès:**

  - **Code:** 200 <br />
    **Contenu:**
    ```json
    [
      {
        "id": 2,
        "description": "Bob",
        "price": 3000,
        "createdAt": "2024-02-13T19:34:34.149Z",
        "updatedAt": "2024-02-13T19:34:34.149Z"
      },
      {
        "id": 3,
        "description": "Bob",
        "price": 3000,
        "createdAt": "2024-02-13T19:37:42.169Z",
        "updatedAt": "2024-02-13T19:37:42.169Z"
      },
      {
        "id": 4,
        "description": "Bob",
        "price": 3000,
        "createdAt": "2024-02-13T19:37:42.972Z",
        "updatedAt": "2024-02-13T19:37:42.972Z"
      },
      {
        "id": 5,
        "description": "Bob",
        "price": 3000,
        "createdAt": "2024-02-13T19:37:43.601Z",
        "updatedAt": "2024-02-13T19:37:43.601Z"
      }
    ]
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
