---
title: Modifier un test ⛔
description: Route pour modifier un test
---

Route pour modifier un test.

- **URL**

  /api/users/{userId}/tests

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
      "user_id": 2,
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
