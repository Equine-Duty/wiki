---
title: Confirmer l'horaire ⛔
description: Route pour confirmer un horaire.
---

Route pour confirmer un horaire.

- **URL**

  /api/shows/{showId}/date/{date}/confirmSchedule

- **Méthode:**

  `POST`

- **Paramètre:**<br>

  Content-Type: application/json

  ```json
  {
    "rings": [
      {
        "name": "allo",
        "start_time": "11:00 JMEN BLC",
        "date": "2024-01-09",
        "ClassSchedule": [
          {
            "number": "123",
            "name": "Jumping Area A",
            "duration_minute": 3,
            "test": "1-1 (SHORT NAME)",
            "riders": [
              {
                "id": 1,
                "name": "Bob",
                "time_start": "08:00",
                "horse": {
                  "name": "Thunder",
                  "id": 1
                }
              }
            ],
            "judges": [
              {
                "name": "Marco",
                "position": "B"
              }
            ]
          }
        ]
      }
    ]
  }
  ```

- **Réponse de succès:**

  - **Code:** 201 Created<br />
    **Contenu:**
    ```json
    { "message": "Votre horaire est confirmé." }
    ```

- **Code d'erreur:**<br>

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

  - **Code:** 400 BAD REQUEST <br />
    **Contenu:**
    ```json
      { "message": "{Message erreur de validation ici}" }
    ```