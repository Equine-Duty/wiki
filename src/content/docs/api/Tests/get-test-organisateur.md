---
title: Recevoir touts les tests d'un organisateur ✅
---

Route pour recevoir tous les tests d'un organisateur.

- **URL**
  /api/users/{userId}/tests

- **Méthode:**

  `GET`

- **Réponse de succès:**
  - **Code:** 200 <br />
    **Contenu:**
    ```json
    [
      {
          "id": 1,
          "number": "Alloa",
          "name": "Jumping Class A",
          "date": "2024-02-01T10:00:00.000Z",
          "ring_name": "Bell Center",
          "ring_number": "12AB",
          "price_entry": 50,
          "show_id": 1,
          "level_type": "Training",
          "is_test_of_choice": false,
          "createdAt": "2024-02-11T22:23:28.693Z",
          "updatedAt": "2024-02-11T22:23:28.693Z"
      },
      {
        ...
      },
    ]
    ```
