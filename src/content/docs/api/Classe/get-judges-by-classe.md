---
title: Obtenir des juges par classses ✅
description: Route pour obtenir des juges par une classe depuis son ID
---

- **URL**

  /api/shows/{showId}/classes/{classId}/judges

- **Méthode:**

  `GET`

- **Réponse de succès:**
  - **Code:** 200 <br />
    **Contenu:**
    ```json
    [
    {
        "id": 1,
        "class_id": 1,
        "name": "John Deer",
        "ring_position": "H",
        "createdAt": "2024-02-15T17:20:38.330Z",
        "updatedAt": "2024-02-15T17:20:38.330Z"
    }
    ]
    ```
 - **Code:** 204 <br />
    **Contenu:**
    ```json
    [
    ]

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

    * **Code:** 400 BAD REQUEST <br />
    **Contenu:** 
    ```json
    { "message": "The show does not own the classe" }
    ```

  * **Code:** 404 NOT FOUND <br />
    **Contenu:** 
    ```json
    { "message": "La ressource n’existe pas." }
    ```
 
