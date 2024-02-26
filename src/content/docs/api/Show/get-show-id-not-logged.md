---
title: Recevoir un show par id (non connecté) ⛔
description: Route pour recevoir un show par son id lorsque le user n'est pas connecté.
---

Route pour recevoir un show par son id lorsque le user n'est pas connecté.

- **URL**

  /api/shows/notLoggedDetails/{showId}

- **Méthode:**

  `GET`

- **Réponse de succès:**

  - **Code:** 200 <br />
    **Contenu:**
    ```json
    {
      "id": 1,
      "name": "Show 1",
      "start_date": "2024-01-06T08:24:24.992Z",
      "end_date": "2025-04-28T14:36:25.664Z",
      "nb_free_place": 68,
      "address": {
        "city": "Montreal",
        "zip_code": "12345"
      }
    }
    ```

- **Réponse d'erreur:**

  - **Code:** 204 No Content <br />
