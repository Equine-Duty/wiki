---
title: Obtenir une classe depuis son ID ✅
description: Route pour obtenir une classe depuis son ID
---

- **URL**

  /api/shows/{showId}/classes/{classId}

- **Méthode:**

  `GET`

- **Réponse de succès:**
  - **Code:** 200 <br />
    **Contenu:**
    ```json
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
    }
    ```

   
* **Réponse d'erreur:**

  * **Code:** 401 UNAUTHORIZED <br />
    **Contenu:** 
    ```json
    { "message": "Non authentifié." }
    ```

  * **Code:** 403 FORBIDDEN <br />
    **Contenu:** 
    ```json
    { "message": "Cette action n’est pas autorisée." }
    ```

  * **Code:** 404 NOT FOUND <br />
    **Contenu:** 
    ```json
    { "message": "La ressource n’existe pas." }
    ```
 
