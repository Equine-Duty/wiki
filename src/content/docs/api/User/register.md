---
title: Register ✅
description: Route pour ajouter un user.
---

Route pour ajouter un user.

* **URL**

  /api/auth/register

* **Méthode:**
  
  `POST`

* **Paramètres:**

  Content-Type: application/json

  **Requis:**
 
    `name=[string]`<br>
    `email=[string]`<br>
    `phone=[string]`<br>
    `password=[string]`<br>
    `birthdate=[string]`<br>

* **Réponse de succès:**

    * **Code:** 201 Created <br />
        **Contenu:** <br>
        `string => User created`

* **Réponse d'erreur:**

    * **Code:** 400 Bad Request <br />
        **Contenu:** 
        ```json
        {
            "name": "ValidationError",
            "message": "Validation Failed",
            "statusCode": 400,
            "error": "Bad Request",
            "details": {
                "body": [
                    {
                        "message": "\"email\" is not allowed to be empty",
                        "path": [
                            "email"
                        ],
                        "type": "string.empty",
                        "context": {
                            "label": "email",
                            "value": "",
                            "key": "email"
                        }
                    }
                ]
            }
        }
        ```

    * **Code:** 400 Bad Request <br />
        **Contenu:**
        ```json
        {"error": "Email already taken"}
        ```
