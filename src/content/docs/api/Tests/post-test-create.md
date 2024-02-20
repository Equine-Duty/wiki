---
title: Ajouter un test avec des marks ⛔
description: Route pour ajouter un test
---

- **URL**

  /api/users/{userId}/tests

- **Méthode:**

  `POST`

- **Paramètres:**

  Content-Type: application/json

  **Requis:**<br>
  `number=[string]`<br>
  `name=[string]`<br>
  `short_name=[string]`<br>
  `points_precision=[int]`<br>
  `duration_minute=[int]`<br>
  `total_points_possibility=[int]`<br>

  **Optionnel**<br>
  `nb_standard_marks=[int]`<br>
  `nb_collectives_marks=[int]`<br>
  `marks=[JsonObjectArray]`<br>
  - `move_name=[string]`
  - `note=[int]`
  - `coef_points=[double]`
  - `type=[string|COLLECTIVE||STANDARD]`

- **Réponse de succès:**

  - **Code:** 201 Created<br />
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
      "createdAt": "2024-02-15T19:07:11.275Z",
      "updatedAt": "2024-02-15T19:07:11.275Z"
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
