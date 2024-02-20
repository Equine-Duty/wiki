---
title: Modifier une marks ⛔
description: Route pour modifier une mark.
---

Route pour modifier une mark.

- **URL**

    /api/users/{userId}/marks/{marksId}

- **Méthode:**

    `PUT`

- **Paramètre:**

    Content-Type: application/json

    **Requis:**<br>
    `move_name=[string]`<br>
    `note=[int]`<br>
    `coef_points=[double]`<br>
    `type=[string|COLLECTIVE||STANDARD]`<br>

- **Réponse de succès:**

    - **Code:** 200 OK <br>
      **Contenu:** <br>
      ```json
      {
        "id": 1,
        "move_name": "JUMP",
        "note": 10,
        "coef_points": 3.3,
        "type": "STANDARD",
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