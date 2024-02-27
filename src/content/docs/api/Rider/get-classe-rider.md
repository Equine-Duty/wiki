---
title: Recevoir la liste des riders d'une classe ✅
description: Route pour recevoir la liste des riders d'une classe
---

Route pour recevoir la liste des riders d'une classe

- **URL**

  /api/classe/{classId}/riders

- **Méthode:**

  `GET`

- **Réponse de succès:**

  - **Code:** 200 <br />
    **Contenu:**
    ```json
    {
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
            "id": 1,
            "name": "Thunder"
          },
          "rider_entry_number": 1,
          "time": 13
        },
        {
          "id": 2,
          "name": "Max Doe",
          "phone": "123-456-7890",
          "email": "max.doe@example.com",
          "no_fei": "FEI789",
          "emergency_name": "Emergency Contact",
          "emergency_phone": "987-654-3210",
          "stable_name": "Stable ABC",
          "trainer_name": "Trainer XYZ",
          "user_id": 1,
          "horse": {
            "id": 1,
            "name": "Thunder"
          },
          "rider_entry_number": 2,
          "time": 13
        }
      ]
    }
    ```

- **Réponse d'erreur:**

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
