---
title: Modifier une classe ✅
description: Route pour modifier une classe
---

Route pour modifier une classe.

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
      "id": 1,
      "number": "a",
      "name": "<nom de la classe>",
      "date": "2024-01-29",
      "ring_name": "<nom du ring>",
      "ring_number": "<numero du ring>",
      "price_entry": 1499,
      "show_id": 1,
      "test_id": 1,
      "level_type": "Master",
      "is_test_of_choice": true,
      "createdAt": "2024-02-13T19:37:53.933Z",
      "updatedAt": "2024-02-13T19:42:55.887Z"
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
