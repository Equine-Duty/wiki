---
title: Recevoir un show par id ✅
description: Route pour recevoir un show par son id
---

- **URL**

  /api/shows/{showId}

- **Méthode:**

  `GET`

- **Réponse de succès:**

  - **Code:** 200 <br />
    **Contenu:**
    ```json
    {
      "id": 1,
      "name": "Show 1",
      "address": {
        "id": 1,
        "street_address": "123 Main Street",
        "province": "Quebec",
        "country": "Canada",
        "zip_code": "12345"
      },
      "organizer": {
        "id": 2,
        "name": "Mark Admio",
        "email": "admin@email.com"
      },
      "secretary": {
        "name": "Astarion Ancunin"
      },
      "Classes": [
        {
          "name": "Jumping Class A"
        }
      ],
      "path_logo": null,
      "nb_free_place": 55,
      "nb_total_place": 91,
      "show_fees": {
        "hay": 50,
        "chiving": 30,
        "permanent_stall_per_day": 15,
        "temp_stall_per_day": 10,
        "tack_stall_per_day": 5,
        "drug_test": 20
      },
     "Shows_Packages": [
        {
            "package": {
                "id": 1,
                "name": "Bundle 1",
                "description": "Big and good bundle",
                "tack_stalls": 2,
                "stalls": 2,
                "hays": 20,
                "chiving": 20,
                "price": 30
            }
        }
    ],
      "nb_free_permanent_stalls": 2,
      "nb_free_temp_stalls": 2,
      "nb_free_tack_stalls": 2,
      "recognized_show": false,
      "rules": "Hello I am the rules!",
      "start_date": "2024-11-24T03:10:52.634Z",
      "end_date": "2026-06-26T18:36:45.584Z",
      "inscription_start_date": "2024-12-16T13:55:34.052Z",
      "inscription_end_date": "2026-11-23T23:29:51.336Z",
      "inscription_end_late_date": "2026-12-26T13:55:59.877Z"
    }
    ```

- **Réponse d'erreur:**

  - **Code:** 404 NOT FOUND <br />
    **Contenu:**
    ```json
    { "message": "La ressource n’existe pas." }
    ```
