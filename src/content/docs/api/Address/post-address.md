---
title: Créer une nouvelle adresse ✅
descripton: Route pour créer une nouvelle adresse.
---

Route pour créer une nouvelle adresse.

- **URL**

  /api/users/{userId}/address

- **Méthode:**

  `POST`

- **Paramètres:**

  **Requis:**

  Content-Type: application/json

  `street_address=[string]`<br>
  `province=[string]`<br>
  `country=[string]`<br>
  `city=[string]`<br>
  `zip_code=[string]`<br>

  **Optionnel:**<br>

  `other_information=[string]`<br>

- **Réponse de succès:**

  - **Code:** 200 <br />
    **Contenu:**
    ```json
    {
      {
        "id": 1,
        "street_address": "123 Main Street",
        "province": "Quebec",
        "country": "Canada",
        "city": "Montreal",
        "zip_code": "12345",
        "other_information": null,
        "organizer_id": 4,
        "createdAt": "2024-02-13T19:11:40.020Z",
        "updatedAt": "2024-02-13T19:11:40.020Z"
      },
    }
    ```

- **Réponse d'erreur:**

  - **Code:** 401 UNAUTHORIZED <br />
    **Contenu:**

    ```json
    { "message": "Non authentifié." }
    ```

  - **Code:** 403 FORBIDDEN <br />
    **Contenu:**
    ```json
    { "message": "Cette action n’est pas autorisée." }
    ```
