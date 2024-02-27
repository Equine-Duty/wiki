---
title: Modifier un résultat ✅
description: Route pour un modifier un résultat.
---

Route pour un modifier un résultat.

- **URL**

  /api/result/test/{testId}/rider/{riderId}

- **Méthode:**

  `PUT`

- **Paramètre:**

  Content-Type: application/json

   **Requis:**<br>

    `score=[number]`<br>
    `nbErrors=[int]`<br>
    `reason=[ELEMINATED|HC|NO_SHOW|RETIRED|SCRATCH|VET_OUT|WITHDREW]`<br>
    `horse_id=[int]`<br>
    `rider_entry_number`<br>

- **Réponse de succès:**

  - **Code:** 201 Created <br>
    **Contenu:**<br>
    ```json
    {
      "score": 50,
      "nbErrors": 1,
      "reason": "RETIRED",
      "horse_id": 1,
      "rider_entry_number": 1
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