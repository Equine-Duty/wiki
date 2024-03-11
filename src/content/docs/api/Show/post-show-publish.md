---
title: Publier un show ✅
description: Route pour publier un show.
---

Route pour publier un show.

- **URL**

  /api/shows/{showId}/publish

- **Méthode:**
  
  `POST`

- **Réponse de succès:**<br>
  
  - **Code:** 200 OK <br>
    **Contenu:**
    ```json
    { "message" : "Le show a été publié avec succès"}
    ```

- **Réponse d'erreur:**

  - **Code:** 401 UNAUTHORIZED <br />
    **Contenu:** 
    ```json
    { "message" : "Non authentifié." }
    ```

  - **Code:** 403 FORBIDDEN <br />
    **Contenu:** 
    ```json
    { "message" : "Cette action n’est pas autorisée." }
    ```