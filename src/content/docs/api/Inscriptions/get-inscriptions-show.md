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
    [
      {
        "id": 1,
        "horse_id": 1,
        "rider_id": 1,
        "show_id": 1,
        "user_id": 1,
        "no_fei": "FEI123",
        "nb_stalls": 2,
        "nb_hay_bale": 5,
        "nb_shaving_bags": 3,
        "has_payed": false,
        "invoice_number": null,
        "approved": false,
        "createdAt": "2024-02-23T16:13:51.608Z",
        "updatedAt": "2024-02-23T16:13:51.608Z",
        "Classes_Inscriptions": [
          {
            "class_id": 1,
            "class": {
              "name": "Jumping Class A"
            }
          }
        ],
        "Inscriptions_Asked_Codes": [
          {
            "code_name": "quebec_equestre",
            "code_value": "1342346"
          }
        ],
        "user": {
          "name": "John Doe"
        },
        "rider": {
          "name": "Jane Doe"
        },
        "horse": {
          "name": "Thunder"
        }
      },
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