---
title: Ajouter un cheval ✅
description: Route pour ajouter un cheval à un user.
---

Route pour ajouter un cheval à un user.

* **URL**

  /api/users/{userId}/horses

* **Méthode:**
  
  `POST`

* **Paramètres:**

    Content-Type: form-data

  **Requis:**
 
    `name=[string]`<br>
    `sex=[string]`<br>
    `email_owner=[string]`<br>
    `name_owner=[string]`<br>
    `phone_owner=[string]`<br>
  
  **Optionnel**<br>
    `no_fei=[string]`<br>
    `no_micro_chip=[string]`<br>
    `vaccine=[.pdf|.png|.jpeg]`<br>
    `coggins=[.pdf|.png|.jpeg]`<br>
    `fei_owner=[string]`<br>

* **Réponse de succès:**
  
  * **Code:** 201 <br />
    **Contenu:** 
    ```json
    {
      "horse": {
          "id": 1,
          "name": "Gourmand",
          "sex": "Female",
          "no_fei": "10333333",
          "path_vaccine": "/vaccine/thunderbolt.pdf",
          "path_coggins": "/coggins/thunderbolt.pdf",
          "user_id": 5
        },
      "owner": {
          "name": "Bob",
          "no_fei": "12345678",
          "email": "Bob@gmail.com",
          "phone": "450-555-6060"
      }
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
