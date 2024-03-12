---
title: Ajouter un rider ✅
description: Route pour ajouter un rider à un user.
---

Route pour ajouter un rider à un user.

- **URL**

  /api/users/{userId}/riders

- **Méthode:**

  `POST`

- **Paramètres:**

  Content-Type: application/json

  **Requis:**

  `name=[string]`<br>
  `phone=[string]`<br>
  `email=[string]`<br>
  `emergency_name=[string]`<br>
  `emergency_phone=[string]`<br>
  `stable_name=[string]`<br>
  `trainer_name=[string]`<br>

  **Optionnel**
  `no_fei=[string]`<br>

- **Réponse de succès:**

  - **Code:** 201 <br />
    **Contenu:**
    ```json
    {
      "id": 1,
      "name": "Alexandra Rider",
      "phone": "450-123-4567",
      "email": "alexandra.rider@example.com",
      "no_fei": "12345678",
      "emergency_name": "John Smith",
      "emergency_phone": "450-987-6543",
      "stable_name": "Majestic Stables",
      "trainer_name": "Emily Trainer",
      "user_id": 1,
      "createdAt": "2024-02-13T20:27:36.747Z",
      "updatedAt": "2024-02-13T20:27:36.747Z"
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
