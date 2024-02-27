---
title: Modifier un test + marks ✅
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
  `marks=[JsonObjectArray]`<br>
  - `move_name=[string]`
  - `note=[int]`
  - `coef_points=[double]`
  - `type=[string|COLLECTIVE||STANDARD]`

- **Réponse de succès:**

  - **Code:** 200 OK <br />
    **Contenu:**
    ```json
    {
      "test": {
          "id": 7,
          "number": " 99",
          "name": " jojo",
          "short_name": " n",
          "points_precision": 77,
          "duration_minute": 88,
          "nb_standard_marks": 3,
          "nb_collectives_marks": 70,
          "total_points_possibility": 100,
          "user_id": 2,
          "createdAt": "2024-02-26T19:33:31.544Z",
          "updatedAt": "2024-02-26T19:35:04.386Z",
          "Marks": [
              {
                  "id": 12,
                  "move_name": "hohoho",
                  "note": 999,
                  "coef_points": 999,
                  "type": "STANDARD",
                  "test_id": 7,
                  "createdAt": "2024-02-26T19:35:04.386Z",
                  "updatedAt": "2024-02-26T19:35:04.386Z"
              },
              {
                  "id": 13,
                  "move_name": "pp",
                  "note": 999,
                  "coef_points": 999,
                  "type": "STANDARD",
                  "test_id": 7,
                  "createdAt": "2024-02-26T19:35:04.386Z",
                  "updatedAt": "2024-02-26T19:35:04.386Z"
              }
          ]
      }
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
