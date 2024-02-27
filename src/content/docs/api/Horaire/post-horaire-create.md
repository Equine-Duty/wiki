---
title: Générer l'horaire ✅
description: Route pour générer un horaire.
---

Route pour générer un horaire.

- **URL**

  /api/shows/{showId}/schedule

- **Méthode:**

  `POST`

- **Paramètre:**<br>

  Content-Type: application/json

- **Réponse de succès:**

  - **Code:** 201 Created<br />
    **Contenu:**
    ```json
    {
      "id": -1,
      "rings": [
        {
          "name": "Bell Center",
          "classes": [
            {
              "number": "Alloa",
              "name": "Jumping Class A",
              "duration_minute": 5,
              "judges": [
                {
                  "name": "John Deer",
                  "position": "H"
                },
                {
                  "name": "Marko Diamo",
                  "position": "B"
                }
              ],
              "test": "BD1",
              "riders": [
                {
                  "time_start": "00:00 AM",
                  "number": 1,
                  "name": "Jane Doe",
                  "horse": {
                    "id": 1,
                    "name": "Thunder"
                  }
                },
                {
                  "time_start": "00:00 AM",
                  "number": 2,
                  "name": "Max Doe",
                  "horse": {
                    "id": 1,
                    "name": "Thunder"
                  }
                }
              ]
            }
          ]
        },
        {
          "name": "Baldurs Center",
          "classes": [
            {
              "number": "1-1",
              "name": "Running Class A",
              "duration_minute": 5,
              "judges": [],
              "test": "BD1",
              "riders": [
                {
                  "time_start": "00:00 AM",
                  "number": 1,
                  "name": "Jane Doe",
                  "horse": {
                    "id": 2,
                    "name": "Electric"
                  }
                },
                {
                  "time_start": "00:00 AM",
                  "number": 1,
                  "name": "Jane Doe",
                  "horse": {
                    "id": 4,
                    "name": "Electric"
                  }
                },
                {
                  "time_start": "00:00 AM",
                  "number": 1,
                  "name": "Jane Doe",
                  "horse": {
                    "id": 2,
                    "name": "Electric"
                  }
                }
              ]
            }
          ]
        },
        {
          "name": "Bell Center",
          "classes": [
            {
              "number": "1-2",
              "name": "Jumping Class B",
              "duration_minute": 5,
              "judges": [],
              "test": "BD1",
              "riders": []
            }
          ]
        }
      ]
    }
    ```

- **Code d'erreur:**<br>

  - **Code:** 400 FORBIDDEN <br />
    **Contenu:**

    ```json
    { "message": "La ressource a déjà été crée" }
    ```

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
