---
title: Ajouter un bundle ✅
description: Route pour ajouter un bundle dans un show
---

Route pour ajouter un bundle dans un show.

* **URL**

  /api/shows/{showId}/bundles

* **Méthode:**
  
  `POST`

* **Paramètres:**

    Content-Type: application/x-www-form-urlencoded

  **Requis:**
 
    `description=[string]`<br>
    `price=[string]`<br>

* **Réponse de succès:**
  
  * **Code:** 201 <br />
    **Contenu:** 
    ```json
    {
        "id": 1,
        "description": "Box and hay",
        "price": 300,
        "createdAt": "2024-02-13T19:34:34.149Z",
        "updatedAt": "2024-02-13T19:34:34.149Z"
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
