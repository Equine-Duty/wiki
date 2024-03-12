---
title: Recevoir les adresses d'un user ✅
description: Route pour recevoir les adresses d'un user
---

Route pour recevoir les adresses d'un user

* **URL**

  /api/users/{userId}/address

* **Méthode:**
  
  `GET`

* **Réponse de succès:**
  
  * **Code:** 200 <br />
    **Contenu:** 
    ```json
    {
      "data": [
        {
          "id": 1,
          "street_address": "123 Main Street",
          "province": "Quebec",
          "country": "Canada",
          "city": "Montreal",
          "zip_code": "12345",
          "other_information": null,
          "organizer_id": 4,
          "createdAt": "2024-02-06T20:40:17.314Z",
          "updatedAt": "2024-02-06T20:40:17.314Z"
        },
        {
          "id": 2,
          "street_address": "123 Rue des Colibris",
          "province": "Quebec",
          "country": "Canada",
          "city": "Saint-Luc",
          "zip_code": "J3Z9P8",
          "other_information": "Porte a droite",
          "organizer_id": 4,
          "createdAt": "2024-02-06T20:44:29.018Z",
          "updatedAt": "2024-02-06T20:44:29.018Z"
        },
        {
          "id": 3,
          "street_address": "123 Rue des Colibris",
          "province": "Quebec",
          "country": "Canada",
          "city": "Saint-Luc",
          "zip_code": "J3Z9P8",
          "other_information": "Porte a droite",
          "organizer_id": 4,
          "createdAt": "2024-02-06T21:19:10.372Z",
          "updatedAt": "2024-02-06T21:19:10.372Z"
        }
      ]
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
