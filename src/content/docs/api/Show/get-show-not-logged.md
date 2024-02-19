---
title: Recevoir la liste des shows pour un utilisateur non connecté ✅
description: Route pour recevoir la liste des show pour un utilisateur non connecté
---

- **URL**

  /api/shows

- **Méthode:**
  
  `GET`

- **Réponse de succès:**
  
  - **Code:** 200 OK <br />
    **Contenu:** 
    ```json
    {
      "data": [{
        "id": 19,
        "name": "Show 19",
        "organizer": {
          "name": "Mark Admio"
        },
        "path_logo": null,
        "nb_free_place": 55,
        "nb_total_place": 76,
        "start_date": "2023-01-10T09:08:34.994Z",
        "end_date": "2025-09-01T23:59:38.135Z",
        "address": {
          "street_address": "123 Main Street",
          "city": "Montreal",
          "province": "Quebec",
          "country": "Canada",
          "zip_code": "12345"
        },
        "pagination": {
          "total_records": 49,
          "current_page": 1,
          "total_pages": 5,
          "next_page": 2,
          "prev_page": null,
        }
      }]
    }
    ```

 * **Code:** 204 <br />
    **Contenu:** 
    ```json
    {"data": "La ressource n'existe pas"}
    ```
* **Réponse d'erreur:**

  * **Code:** 404 NOT FOUND <br />
    **Contenu:** 
    ```json
    { "message": "La ressource n’existe pas." }
    ```