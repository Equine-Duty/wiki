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
        {
          "id": 3,
          "name": "Show 3",
          "start_date": "2023-01-21T13:29:37.056Z",
          "end_date": "2026-12-12T08:48:17.163Z",
          "nb_free_place": 90,
          "organizer": {
            "name": "Mark Admio"
          },
          "address": {
            "city": "Montreal",
            "zip_code": "12345"
          }
        },
        {
          "id": 43,
          "name": "Show 43",
          "start_date": "2023-01-24T08:10:07.219Z",
          "end_date": "2024-04-10T22:44:16.360Z",
          "nb_free_place": 96,
          "organizer": {
            "name": "Mark Admio"
          },
          "address": {
            "city": "Montreal",
            "zip_code": "12345"
          }
        },
      }],
      "pagination": {
          "total_records": 49,
          "current_page": 1,
          "total_pages": 5,
          "next_page": 2,
          "prev_page": null,
      }
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