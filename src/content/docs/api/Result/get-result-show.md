---
title: Recevoir tout les résultats d'un show ⛔
description: Route pour recevoir tout les résultats d'un show.
---

Route pour recevoir tout les résultats d'un show.

- **URL**

  /api/results/shows/{showId}

- **Méthode:**

  `GET`

- **Réponse de succès:**

  - **Code:** 200 OK <br>
  **Contenu:**
  ```json
  {
    "show": {
      "name": "Show 1",
      "start_date": "2023-08-02T16:54:55.361Z",
      "classes": [
        {
          "name": "Jumping Class A",
          "number": "Alloa",
          "test": {
            "name": "Basic Test",
            "Results": [
              {
                "rider_name": "Jane Doe",
                "horse_name": "Thunder",
                "score": 70,
                "rider_entry_number": 1
              },
              {
                "rider_name": "Jane Doe",
                "horse_name": "Thunder",
                "score": 50,
                "rider_entry_number": 1
              },
              {
                "rider_name": "Jane Doe",
                "horse_name": "Thunder",
                "score": 20,
                "rider_entry_number": 1
              }
            ]
          }
        }
      ]
    }
  }
  ```

- **Réponse d'erreur:**

  - **Code:** 204 No Content