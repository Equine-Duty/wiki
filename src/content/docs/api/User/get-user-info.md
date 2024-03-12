---
title: Recevoir les infos d'un user par son id ✅
description: Route pour recevoir les infos d'un user.
---

Route pour recevoir les infos d'un user.

* **URL**

  /api/users/{userId}

* **Méthode:**
  
  `GET`

* **Réponse de succès:**
  
  * **Code:** 200 <br />
    **Contenu si rôle du jwt est USER:** 
    ```json
    {
      "id": 1,
      "name": "James Cameron",
      "email": "james04@gmail.com",
      "phone": "4508699045",
      "birthdate": "1992-07-03",
    }
    ```
    
    **Contenu si rôle du jwt est ADMIN:** 
    ```json
    {
      "id": 1,
      "name": "James Cameron",
      "email": "james04@gmail.com",
      "phone": "4508699045",
      "birthdate": "1992-07-03", 
      "role": "USER",
      "is_verified": true,
      "createdAt": "2024-02-08T21:13:53.948Z",
      "updatedAt": "2024-02-08T21:13:53.948Z",
      "stripe_connected": true,
    }
    ```

    **Contenu si rôle du jwt est ORGANIZER:** 
    ```json
    {
      "id": 1,
      "name": "James Cameron",
      "email": "james04@gmail.com",
      "phone": "4508699045",
      "birthdate": "1992-07-03", 
      "role": "USER",
      "is_verified": true,
      "createdAt": "2024-02-08T21:13:53.948Z",
      "updatedAt": "2024-02-08T21:13:53.948Z",
      "remaining_show": 5,
      "stripe_connected": true,
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
