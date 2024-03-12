---
title: Recevoir une inscription par son id ✅
description: Route pour recevoir une inscription par son id.
---

Route pour recevoir une inscription par son id.

- **URL**

  /api/shows/{showId}/classes/{classId}/inscriptions/{inscriptionId}

- **Méthode:**

  `GET`

- **Réponse de succès:**
  - **Code:** 200 OK <br>
  **Contenu:** <br>
  ```json
  {
    "id": 1,
    "horse_id": 1,
    "rider_id": 1,
    "show_id": 1,
    "user_id": 1,
    "no_fei": "FEI123",
    "nb_stalls": 2,
    "nb_tack_stalls": 1,
    "nb_hay_bale": 5,
    "nb_chiving_bags": 3,
    "stall_type": "PERMANENT",
    "has_payed": false,
    "invoice_number": null,
    "approved": false,
    "createdAt": "2024-02-26T13:33:57.418Z",
    "updatedAt": "2024-02-26T13:33:57.418Z",
    "Inscriptions_Asked_Codes": [
      {
        "id": 1,
        "code_name": "quebec_equestre",
        "inscription_id": 1,
        "code_value": "1342346",
        "createdAt": "2024-02-26T13:33:57.452Z",
        "updatedAt": "2024-02-26T13:33:57.452Z"
      }
    ],
    "show": {
      "id": 1,
      "name": "Show 1",
      "start_date": "2023-08-04T17:24:16.086Z",
      "city": "Montreal",
      "zip_code": "12345"
    },
    "horse_name": "Thunder",
    "rider_name": "Jane Doe",
    "show_asked_codes": [
      {
        "id": 1,
        "code_name": "quebec_equestre",
        "inscription_id": 1,
        "code_value": "1342346",
        "createdAt": "2024-02-26T13:33:57.452Z",
        "updatedAt": "2024-02-26T13:33:57.452Z"
      }
    ],
    "class_name": "Jumping Class A",
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