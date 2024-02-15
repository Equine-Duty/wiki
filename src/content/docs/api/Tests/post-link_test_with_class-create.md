---
title: Ajouter une classe dans un test ✅
description: Route pour ajouter une classe dans un test
---

- **URL**

  /api/users/:userId/tests/:testId/class/:classId

- **Méthode:**

  `PUT`

- **Paramètres:**

  Content-Type: application/json

- **Réponse de succès:**

  - **Code:** 200 <br />
    **Contenu:**
    ```json
    {
        "id": 1,
        "number": "Alloa",
        "name": "Jumping Class A",
        "date": "2024-02-01T10:00:00.000Z",
        "ring_name": "Bell Center",
        "ring_number": "12AB",
        "price_entry": 50,
        "show_id": 1,
        "test_id": 2,
        "level_type": "Training",
        "is_test_of_choice": false,
        "createdAt": "2024-02-15T17:20:38.312Z",
        "updatedAt": "2024-02-15T19:49:22.993Z"
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
