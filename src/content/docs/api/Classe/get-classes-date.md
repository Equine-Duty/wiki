---
title: Obtenir une classe pour un show et une date  ✅
description: Route pour obtenir une classe depuis un show et sa date. Pour organisateurs et admins.
---

- **URL**

  /api/shows/adminShows/{showId}/classes/date/{date}

- **EXEMPLE**
  /api/shows/adminShows/1/classes/date/2024-01-02

- **Méthode:**

  `GET`

- **Réponse de succès:**
  - **Code:** 200 <br />
    **Contenu:**

```json
{
  "is_schedule": true,
  "data": {
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
                  "id": 1,
                  "name": "BREAK"
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
      },
      {
        "name": "new ring",
        "start_time": "13:00 JMEN BLC",
        "date": "2024-01-09",
        "ClassSchedule": [
          {
            "number": "456",
            "name": "Jumping Area B",
            "duration_minute": 4,
            "test": "2-1 (SHORT NAME)",
            "riders": [
              {
                "id": 1,
                "name": "Alice",
                "time_start": "08:50",
                "horse": {
                  "id": 1,
                  "name": "BREAK"
                }
              }
            ],
            "judges": [
              {
                "name": "Maria",
                "position": "B"
              }
            ]
          },
          {
            "number": "1-2",
            "name": "Jumping Area B",
            "duration_minute": 4,
            "test": "2-1 (SHORT NAME)",
            "riders": [
              {
                "id": 1,
                "name": "Alice",
                "time_start": "08:50",
                "horse": {
                  "id": 1,
                  "name": "BREAK"
                }
              }
            ],
            "judges": [
              {
                "name": "Maria",
                "position": "B"
              }
            ]
          }
        ]
      }
    ],
    "classes": [
      {
        "id": 4,
        "number": "asd",
        "name": "asd",
        "duration_minute": 5,
        "test": "BD1",
        "riders": [
          {
            "id": 1,
            "name": "Jane Doe",
            "time_start": "-00:00 AM",
            "horse": {
              "id": 2,
              "name": "Electric"
            }
          }
        ],
        "judges": [
          {
            "id": 1,
            "class_id": 4,
            "ring_name": "Bell Center",
            "name": "John Deer",
            "ring_position": "H",
            "createdAt": "2024-02-29T02:03:43.457Z",
            "updatedAt": "2024-02-29T02:03:43.457Z"
          }
        ]
      }
    ]
  }
}
```

** SI UN HORAIRE EXISTE **

- **Code:** 200 <br />
  **Contenu:**

  ```json
  {
    "is_schedule": true,
    "data": {
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
                    "id": 1,
                    "name": "BREAK"
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
        },
        {
          "name": "new ring",
          "start_time": "13:00 JMEN BLC",
          "date": "2024-01-09",
          "ClassSchedule": [
            {
              "number": "456",
              "name": "Jumping Area B",
              "duration_minute": 4,
              "test": "2-1 (SHORT NAME)",
              "riders": [
                {
                  "id": 1,
                  "name": "Alice",
                  "time_start": "08:50",
                  "horse": {
                    "id": 1,
                    "name": "BREAK"
                  }
                }
              ],
              "judges": [
                {
                  "name": "Maria",
                  "position": "B"
                }
              ]
            },
            {
              "number": "1-2",
              "name": "Jumping Area B",
              "duration_minute": 4,
              "test": "2-1 (SHORT NAME)",
              "riders": [
                {
                  "id": 1,
                  "name": "Alice",
                  "time_start": "08:50",
                  "horse": {
                    "id": 1,
                    "name": "BREAK"
                  }
                }
              ],
              "judges": [
                {
                  "name": "Maria",
                  "position": "B"
                }
              ]
            }
          ]
        }
      ],
      "classes": [
        {
          "id": 4,
          "number": "asd",
          "name": "asd",
          "duration_minute": 5,
          "test": "BD1",
          "riders": [
            {
              "id": 1,
              "name": "Jane Doe",
              "phone": "123-456-7890",
              "email": "jane.doe@example.com",
              "no_fei": "FEI456",
              "emergency_name": "Emergency Contact",
              "emergency_phone": "987-654-3210",
              "stable_name": "Stable ABC",
              "trainer_name": "Trainer XYZ",
              "user_id": 1,
              "horse": {
                "id": 2,
                "name": "Electric"
              },
              "rider_entry_number": 6,
              "time": 13
            }
          ],
          "judges": [
            {
              "id": 1,
              "class_id": 4,
              "ring_name": "Bell Center",
              "name": "John Deer",
              "ring_position": "H",
              "createdAt": "2024-02-29T02:03:43.457Z",
              "updatedAt": "2024-02-29T02:03:43.457Z"
            }
          ]
        }
      ]
    }
  }
  ```

  - **Code:** 204 <br />
    **Contenu:**

* **Réponse d'erreur:**

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

  - **Code:** 404 NOT FOUND <br />
    **Contenu:**
    ```json
    { "message": "La ressource n’existe pas." }
    ```
