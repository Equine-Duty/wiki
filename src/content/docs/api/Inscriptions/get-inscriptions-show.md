---
title: Recevoir les inscriptions d'un show ⛔
description: Route pour recevoir toutes les inscriptions d'un show.
---

Route pour recevoir toutes les inscriptions d'un show.

- **URL**

  /api/shows/{showId}/inscriptions <br>
  /api/shows/{showId}/inscriptions?<variable=value> <br>

- **Méthode:**

  `GET`

- **Paramètres:**

  filtre :

  - Variable: `has_payed`

- **Réponse de succès:**
  - **Code:** 200 OK <br>
  **Contenu:** <br>
  ```json
  {
    "inscriptions": [
      {
        "id": 1,
        "horse_id": 1,
        "rider_id": 1,
        "show_id": 1,
        "user_id": 1,
        "no_fei": null,
        "nb_stalls": 45,
        "nb_hay_bale": 30,
        "nb_shaving_bags": 43,
        "has_payed": false,
        "approved": false,
        "class_id": 1,
        "total": 515
      }
      ...
    ]
  }
  ```

- **Réponse d'erreur:**

  - **Code:** 204 No Content<br />

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