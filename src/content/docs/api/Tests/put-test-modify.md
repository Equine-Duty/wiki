---
title: Modifier un test + marks ⛔
description: Route pour modifier un test et ses marks
---

Route pour modifier un test et ses marks.

- **URL**

  /api/users/{userId}/tests/{testId}

- **Méthode:**

  `PUT`

- **Paramètres:**

  Content-Type: application/json<br>

  `number=[string]`<br>
  `name=[string]`<br>
  `short_name=[string]`<br>
  `points_precision=[int]`<br>
  `duration_minute=[int]`<br>
  `total_points_possibility=[int]`<br>
  `nb_standard_marks=[int]`<br>
  `nb_collectives_marks=[int]`<br>
  `Marks=[JsonObjectArray]`<br>
  - `move_name=[string]`
  - `note=[int]`
  - `coef_points=[double]`
  - `type=[string|COLLECTIVE||STANDARD]`

- **Réponse de succès:**

  - **Code:** 200 OK <br />
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

  - **Code:** 401 UNAUTHORIZED <br />
    **Contenu:**
    ```json
    { "message" : "Non authentifié." }
    ```

  - **Code:** 403 FORBIDDEN <br />
    **Contenu:**
    ```json
    { "message" : "Cette action n’est pas autorisée." }
    ```
