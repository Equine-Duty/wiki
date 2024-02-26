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
      "start_date": "2024-11-24T03:10:52.634Z",
      "classes": [
        {
          "name": "Jumping Class A",
          "number": "12",
          "tests": [
            {
              "name": "1-1",
              "results": [
                { // Ordre croissant
                  "rider_name": "Albert",
                  "horse_name": "Rudolph",
                  "entry_number": 1,
                  "score": 98.9,
                }
              ],
            },
          ],
        },
      ],
      }
  }
  ```

- **Réponse d'erreur:**

  - **Code:** 204 No Content