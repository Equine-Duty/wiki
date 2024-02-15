---
title: Ajouter une mark 🛑
description: Route pour ajouter une mark à un test
---

- **URL**

  /api//users/:userId/test/:testId/mark'

- **Méthode:**

  `POST`

- **Paramètres:**

  Content-Type: application/json

  **Requis:**<br>
  `move_name=[string]`<br>
  `note=[int]`<br>
  `coef_points=[double]`<br>
  `type=[string|COLLECTIVE||STANDARD]`<br>

- **Réponse de succès:**

  - **Code:** 201 <br />
    **Contenu:**
    ```json
    {
            "id": 1,
            "move_name": "JUMP",
            "note": 10,
            "coef_points": 3.3,
            "type": "STANDARD",
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

    **Code:** 403 UNAUTHORIZED <br />
    **Contenu:**
    ```json
    { "message": "Count of mark_standard is full" }
    ```

    **Code:** 403 UNAUTHORIZED <br />
    **Contenu:**
    ```json
    { "message": "Count of mark_collective is full" }
    ```

  - **Code:** 403 FORBIDDEN <br />
    **Contenu:**
    ```json
    { "message": "Cette action n’est pas autorisée." }
    ```
