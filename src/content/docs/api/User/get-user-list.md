---
title: Recevoir la liste des users ⛔
---

Route pour recevoir la liste des users avec ou sans filtre.

* **URL**

  /api/users
  /api/users?`<Variable>=<Value>`
  /api/users?`<Variable>=<Value>&page=<Page_Number>`

* **Méthode:**
  
  `GET`

- **Paramètres:**

  filtre :

  - Variable: `name` (Recherche par nom)
  - Variable: `email` (Recherche par email)
  - Variable: `role` (Recherche par role)
    - USER
    - SECRETARY
    - ORGANIZER
    - ADMIN

* **Réponse de succès:**
  
  * **Code:** 200 <br />
    **Contenu:** 
    ```json
    {
      "userslist": [
        {
          "id": 1,
          "name": "John Doe",
          "email": "user@email.com",
          "phone": "123-456-7890",
          "role": "USER"
        },
        {
          "id": 2,
          "name": "Mark Admio",
          "email": "admin@email.com",
          "phone": "123-456-1234",
          "role": "ADMIN"
        },
        {
          "id": 3,
          "name": "Astarion Ancunin",
          "email": "secretary@email.com",
          "phone": "123-987-123",
          "role": "SECRETARY"
        },
        {
          "id": 4,
          "name": "Lola Sapristi",
          "email": "organizer@email.com",
          "phone": "123-987-123",
          "role": "ORGANIZER"
        }
      ],
      "pagination": {
        "total_records": 4,
        "current_page": 1,
        "total_pages": 1,
        "next_page": null,
        "prev_page": null
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

  * **Code:** 404 NOT FOUND <br />
    **Contenu:** 
    ```json
    { "message": "La ressource n’existe pas." }
    ```
