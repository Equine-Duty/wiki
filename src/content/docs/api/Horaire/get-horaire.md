---
title: Obtenir l'horaire imprimable ⛔
description: Route pour obtenir l'horaire imprimable
---

Route pour obtenir l'horaire imprimable.

- **URL**

  /api/shows/{showId}/schedule

- **Méthode:**

  `GET`

- **Paramètre:**<br>

  Content-Type: application/json

- **Type**  
  ```typescript
  type Schedule = {
    id: number;
    dates: {
      date: string;
      rings: Ring[];
    }[]
  };

  type Judge = {
    name: string;
    position: string;
  };

  type Rider = {
    time_start: string;
    number: string | number;
    name: string;
    horse_name: string;
  };

  type EventBreak = {
    time_start: string;
    break_type: "LUNCH" | "BREAK" | "CHANGE RING";
    reason?: string;
  };

  type RidingClass = {
    number: string | number;
    name: string;
    judges: Judge[];
    test: string;
    riders: (Rider | EventBreak)[];
  };

  type Ring = {
    name: string;
    number: string;
    classes: RidingClass[];
  };

  ```

- **Réponse de succès:**
  
  - **Code:** 200 OK<br />
    **Contenu:**
  ```json
  {
    "id": 1,
    "dates": [
      {
        "date": "2023-07-08",
        "rings": [
          {
            "name": "RING",
            "number": "1",
            "classes": [
              {
                "number": "1209",
                "name": "BRONZE - Niveau 1 Adulte Test 1",
                "judges": [
                  {
                    "name": "Francine Bell",
                    "position": "C"
                  },
                  {
                    "name": "Joanie Leclerc",
                    "position": "B"
                  },
                  {
                    "name": "Lili Jade",
                    "position": "A"
                  }
                ],
                "test": "1-1",
                "riders": [
                  {
                    "time_start": "8:00 AM",
                    "number": "45",
                    "name": "Sarah Gibault",
                    "horse_name": "MAGNUM"
                  },
                  {
                    "time_start": "8:07 AM",
                    "number": "28",
                    "name": "Erica David",
                    "horse_name": "BUZZIN"

                  },
                  {
                    "time_start": "8:14 AM",
                    "break_type": "LUNCH"
                  },
                  {
                    "time_start": "8:14 AM",
                    "number": "65",
                    "name": "Joanie Leclerc",
                    "horse_name": "LEGEND"
                  },
                  {
                    "time_start": "8:21 AM",
                    "number": "98",
                    "name": "Lili Jade",
                    "horse_name": "KIRIKOU"
                  }
                ]
              },
              {
                "number": "1209",
                "name": "BRONZE - Niveau 1 Junior Test 1",
                "judges": [
                  {
                    "name": "Francine Bell",
                    "position": "C"
                  },
                  {
                    "name": "Joanie Leclerc",
                    "position": "B"
                  }
                ],
                "test": "1-1",
                "riders": [
                  {
                    "time_start": "8:28 AM",
                    "number": "26",
                    "name": "Florence Cyr",
                    "horse_name": "MISS KHALI"
                  }
                ]
              },
              {
                "number": "211",
                "name": "OR - Niveau 1 Adulte Amateur Test 1",
                "judges": [
                  {
                    "name": "Francine Bell",
                    "position": "C"
                  }
                ],
                "test": "1-1",
                "riders": [
                  {
                    "time_start": "8:35 AM",
                    "number": "7",
                    "name": "Andree Bessette",
                    "horse_name": "FANI DE LYS"
                  },
                  {
                    "time_start": "8:14 AM",
                    "break_type": "BREAK",
                    "reason": "2EME JUGE"
                  },
                  {
                    "time_start": "8:42 AM",
                    "number": "73",
                    "name": "Justine Paré",
                    "horse_name": "ZULLA'S FIRE N ICE"
                  },
                  {
                    "time_start": "8:49 AM",
                    "number": "69",
                    "name": "Sarah Nault",
                    "horse_name": "CALISTA"
                  }
                ]
              }
            ]
          }
        ]
      }
    ]
  }
  ```

- **Code d'erreur:**<br>
  - **Code:** 204 No Content<br />
    **Contenu:**<br>
    ```json
    { "message" : "There is no schedule available for this show"}
    ```

  - **Code:** 401 UNAUTHORIZED <br />
    **Contenu:** 
    ```json
    { "message" : "Non authentifié." }
    ```

  - **Code:** 403 FORBIDDEN <br />
    **Contenu:** 
    ```json
    { "message" : "Cette action n’est pas autorisée." }
    ```
