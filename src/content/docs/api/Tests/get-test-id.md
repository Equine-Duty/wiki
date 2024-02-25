---
title: Recevoir un test par son id avec les marks ⛔
description: Route pour recevoir un test par son id avec les marks associés
---

Route pour recevoir un test par son id avec les marks associés.

- **URL**

  /api/users/{userId}/tests/{testId}

- **Méthode:**

  `GET`

- **Réponse de succès:**

  - **Code:** 200 OK <br>
    **Contenu:**
    ```json
    {
      "id": 2,
      "number": "12",
      "name": "Allo",
      "short_name": "A",
      "points_precision": 13,
      "duration_minute": 20,
      "nb_standard_marks": 25,
      "nb_collectives_marks": 25,
      "total_points_possibility": 50,
      "user": {
        "id": 4
      },
      "Marks": [
        {
          "id": 1,
          "move_name": "JUMP",
          "note": 2,
          "coef_points": 3.3,
          "type": "COLLECTIVE",
        }
        ...
      ]
    }
    ```

- **Réponse d'erreur:**

  - **Code:** 204 No Content <br />

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