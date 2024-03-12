---
title: Recevoir un riders d'un user ✅
description: Route pour recevoir un rider à partir d'un user.
---

Route pour recevoir un rider à partir d'un user.

- **URL**

  /api/users/{userId}/riders/{riderId}

- **Méthode:**

  `GET`

- **Réponse de succès:**

  - **Code:** 200 <br />
    **Contenu:**
    ```json
    {
      "id": 1,
      "name": "Alexandra Rider",
      "phone": "450-123-4567",
      "email": "alexandra.rider@example.com",
      "no_fei": "12345678",
      "emergency_name": "John Smith",
      "emergency_phone": "450-987-6543",
      "stable_name": "Majestic Stables",
      "trainer_name": "Emily Trainer",
      "user_id": 1,
      "createdAt": "2024-02-13T20:03:07.984Z",
      "updatedAt": "2024-02-13T20:03:07.984Z"
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
