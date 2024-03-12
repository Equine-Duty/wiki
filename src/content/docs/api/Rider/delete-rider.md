---
title: Suprimer un rider ✅
description: Route pour supprimer un rider à un user.
---

Route pour supprimer un rider à un user.

- **URL**

  /api/users/{userId}/riders/{riderId}

- **Méthode:**

  `DELETE`

- **Réponse de succès:**

  - **Code:** 200 <br />
    **Contenu:**
    ```json
    {
      "id": 2,
      "name": "AL",
      "phone": "2",
      "email": "2@",
      "no_fei": "2",
      "emergency_name": "2",
      "emergency_phone": "2",
      "stable_name": "2",
      "trainer_name": "2",
      "user_id": 1,
      "createdAt": "2024-02-13T20:03:07.984Z",
      "updatedAt": "2024-02-13T20:03:07.984Z"
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

  - **Code:** 404 NOT FOUND <br />
    **Contenu:**
    ```json
    { "message": "La ressource n’existe pas." }
    ```
