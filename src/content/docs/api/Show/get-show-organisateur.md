---
title: Recevoir touts les shows d'un organisateur ✅
---

Route pour recevoir touts les shows qu'un organisateur a créé.

**URL**

  /api/shows/adminShows
  
- **Méthode:**

  `GET`

- **Paramètres:**


- **Réponse de succès:**

  - **Code:** 200 <br />
    **Contenu:**
     ```json
    {
      "data": [{
        "id": 1,
        "name": "Show 1",
        "organizer": {
          "name": "Mark Admio"
        },
        "nb_free_permanent_stalls": 2,
        "nb_free_temp_stalls": 2,
        "nb_free_tack_stalls": 2,
        "path_logo": null,
        "nb_free_place": 29,
        "nb_total_place": 97,
        "start_date": "2022-06-28T11:58:34.990Z",
        "end_date": "2025-11-11T08:03:03.395Z",
        "address": {
          "street_address": "123 Main Street",
          "city": "Montreal",
          "province": "Quebec",
          "country": "Canada",
          "zip_code": "12345"
        }
      },
      {
        "id": 2,
        "name": "Show 2",
        "organizer": {
          "name": "Mark Admio"
        },
        "path_logo": null,
        "nb_free_place": 78,
        "nb_total_place": 61,
        "start_date": "2023-06-24T18:11:12.735Z",
        "end_date": "2025-04-14T00:10:02.140Z",
        "address": {
          "street_address": "123 Main Street",
          "city": "Montreal",
          "province": "Quebec",
          "country": "Canada",
          "zip_code": "12345"
        }
      }],
    }
    ```
**Réponse d'erreur:**

  - **Code:** 404 NOT FOUND <br />
    **Contenu:**
    ```json
    { "message": "La ressource n’existe pas." }
    ```
	- **CODE** 401 UNAUTHORIZED <br />
	**CONTENU:**<br>
  `string => UNAUTHORIZED`
	  