---
title: Modifier une classe ✅
description: Route pour modifier uneclasse
---

- **URL**

  /api/shows/{showId}/classes/{classId}

- **Méthode:**

  `PUT`

- **Paramètres:**

  **Requis:**

  Content-Type: application/x-www-form-urlencoded

  `number=[string]`<br>
  `name=[string]`<br>
  `date=[date]`<br>
  `ring_name=[string]`<br>
  `ring_number=[string]`<br>
  `price_entry=[int]`<br>
  `level_type=[string]`<br>
  `is_test_of_choice=[bool]`<br>
  `test_id=[int]`<br>
  `judges=[JsonObjectArray]`<br>
  - `ring_name=[string]`
  - `name=[string]`
  - `ring_position=[E|H|C|M|B]`

- **Réponse de succès:**

  - **Code:** 201 <br />
    **Contenu:**
    ```json
     {
      "id": 5,
      "number": "52",
      "name": " 99",
      "date": "2025-01-29T00:00:00.000Z",
      "ring_name": " \"Bell Center\",",
      "ring_number": " \"12AB\",",
      "price_entry": 50,
      "show_id": 1,
      "test_id": 2,
      "level_type": " Training,",
      "is_test_of_choice": true,
      "createdAt": "2024-02-27T20:32:16.532Z",
      "updatedAt": "2024-02-27T20:32:16.532Z",
      "test": {
          "id": 2,
          "number": "AFG123",
          "name": "Basic Test",
          "short_name": "BD1",
          "points_precision": 2,
          "duration_minute": 42,
          "nb_standard_marks": 6,
          "nb_collectives_marks": 4,
          "total_points_possibility": 432,
          "user_id": 2,
          "createdAt": "2024-02-27T20:23:13.135Z",
          "updatedAt": "2024-02-27T20:23:13.135Z"
      },
      "Judges_Classes": [
          {
              "id": 4,
              "class_id": 5,
              "ring_name": "Allo",
              "name": "A",
              "ring_position": "H",
              "createdAt": "2024-02-27T20:32:16.532Z",
              "updatedAt": "2024-02-27T20:32:16.532Z"
          },
          {
              "id": 5,
              "class_id": 5,
              "ring_name": "Allo",
              "name": "Bob",
              "ring_position": "C",
              "createdAt": "2024-02-27T20:32:16.532Z",
              "updatedAt": "2024-02-27T20:32:16.532Z"
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
  - **Code:** 403 FORBIDDEN <br />
    **Contenu:**
    ```json
    {"error": "Test id not found"}
    ```
