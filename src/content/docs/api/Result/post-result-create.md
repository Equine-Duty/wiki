---
title: Ajouter un résultat ✅
description: Route pour ajouter un résultat.
---

Route pour ajouter un résultat.

- **URL**

  /api/result/test/{testId}/rider/{riderId}

- **Méthode:**

  `POST`

- **Paramètre:**

  Content-Type: application/json

  **Requis:**<br>

    `score=[number]`<br>
    `nbErrors=[int]`<br>
    `reason=[ELEMINATED|HC|NO_SHOW|RETIRED|SCRATCH|VET_OUT|WITHDREW]`<br>
    `horse_id=[int]`<br>

- **Réponse de succès:**

  - **Code:** 201 Created <br>
    **Contenu:**<br>
    ```json
    { 
      "score": 20,
      "nbErrors": 2,
      "reason": "RETIRED",
      "horse_id": 1,
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