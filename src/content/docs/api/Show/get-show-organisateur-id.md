---
title: Recevoir un show par id pour un organisateur ✅
description: Route pour recevoir un show par son id pour un un organisateur.
---

Route pour recevoir un show par son id pour un un organisateur.

- **URL**

  /api/shows/adminShows/{showId}

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
      "nb_temp_stalls": 17,
      "nb_permanent_stalls": 17,
      "nb_tack_stalls": 20,
      "organizer": {
        "id": 2,
        "name": "Mark Admio",
        "email": "admin@email.com",
        "phone": "123-456-1234",
        "birthdate": "1990-01-01T00:00:00.000Z"
      },
      "path_logo": null,
      "nb_free_place": 26,
      "nb_total_place": 182,
      "show_fees": {
        "id": 1,
        "hay": 50,
        "shaving": 30,
        "permanent_stall_per_day": 15,
        "temp_stall_per_day": 10,
        "tack_stall_per_day": 5,
        "drug_test": 20
      },
      "administration_fee": {
        "id": 1,
        "administration": 100,
        "late_inscription": 20,
        "cancel_inscription": 30,
        "ground": 50,
        "paramedics": 10,
        "camper_ground_rental": 15
      },
      "Shows_Packages": [
        {
          "id": 1
        }
      ],
      "secretary": {
        "name": "Astarion Ancunin",
        "email": "secretary@email.com",
        "phone": "123-987-123",
        "birthdate": "1990-01-01T00:00:00.000Z"
      },
      "Classes": [
        {
          "id": 1,
          "name": "Jumping Class A",
          "test": {
            "id": 1,
            "name": "Basic Test",
            "Judges_Tests": [
              {
                "id": 1,
                "name": "John Deer",
                "ring_position": "H",
                "ring_name": "Bell Center"
              }
            ]
          }
        }
      ],
      "show_aksed_code": [
        {
          "asked_code_name": "ABC123"
        }
      ],
      "recognized_show": true,
      "rules": "Hello I am the rules!",
      "start_date": "2023-07-08T21:14:58.025Z",
      "end_date": "2024-06-25T01:23:21.833Z",
      "is_vaccination_proof_required": true,
      "is_coggins_proof_required": true,
      "is_published": false,
      "inscription_start_date": "2024-02-25T05:26:06.649Z",
      "inscription_end_date": "2025-05-12T23:33:07.092Z",
      "inscription_end_late_date": "2026-08-08T10:34:53.099Z"
    }
    ```

- **Réponse d'erreur:**

  - **Code:** 404 NOT FOUND <br />
    **Contenu:**
    ```json
    { "message": "La ressource n’existe pas." }
    ```

- **Code:** 401 UNAUTHORIZED <br />
  **CONTENU**:
  ```json
  { "message": "Unauthorized" }
  ```
- **Code:** 403 FORBIDDEN <br />
  **CONTENU**:
  ```json
  { "message": "Forbidden" }
  ```
