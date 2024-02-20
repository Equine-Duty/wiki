---
title: Suprimer une marks ⛔
description: Route pour supprimer une mark.
---

Route pour supprimer une mark.

- **URL**

  /api/users/{userId}/test/{testId}/marks/{markId}

- **Méthode:**

  `DELETE`

- **Réponse de succès:**

  - **Code:** 200 <br />
    **Contenu:**
    ```json
    { "message": "La mark a été supprimé avec succès."}
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
