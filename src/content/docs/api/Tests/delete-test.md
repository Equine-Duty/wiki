---
title: Supprimer un test ⛔
description: Route pour supprimer un test
---

Route pour supprimer un test.

- **URL**

  /api/users/{userId}/tests/{testId}

- **Méthode:**

  `DELETE`

- **Réponse de succès:**

  - **Code:** 200 OK <br />
    **Contenu:**
    ```json
    { "message" : "Le test a été supprimé avec succès."}
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
