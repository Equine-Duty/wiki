---
title: Recevoir la liste des chevaux d'un user ✅
description: Route pour recevoir la liste des chevaux d'un user.
---

Route pour recevoir la liste des chevaux d'un user.

* **URL**

  /api/users/{userId}/horses

* **Méthode:**
  
  `GET`

* **Réponse de succès:**


* **Code:** 204. Si il n'y a pas de ressource<br />
  
* **Code:** 200 <br />
    **Contenu:** 
    ```json
    {
     [
        {
            "id": 1,
            "name": "Thunder",
            "sex": "Male",
            "no_fei": "FEI123",
            "no_micro_chip": "MICROCHIP123",
            "path_vaccine": "/path/to/vaccine_record.pdf",
            "path_coggins": "/path/to/coggins_record.pdf",
            "name_owner": "Bob",
            "fei_owner": "FEI321",
            "email_owner": "Bob@gmail.com",
            "phone_owner": "132-456-1254",
            "createdAt": "2024-02-13T19:06:21.262Z",
            "updatedAt": "2024-02-13T19:06:21.262Z",
            "user_id": 1
        },
        {
            "id": 2,
            "name": "Allo",
            "sex": "Female",
            "no_fei": "FEI123",
            "no_micro_chip": "MICROCHIP123",
            "path_vaccine": null,
            "path_coggins": null,
            "name_owner": "Bob",
            "fei_owner": "FEI321",
            "email_owner": "Bob@gmail.com",
            "phone_owner": "132-456-1254",
            "createdAt": "2024-02-13T19:06:21.262Z",
            "updatedAt": "2024-02-13T19:06:21.262Z",
            "user_id": 1
        }
        ...
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
