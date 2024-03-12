---
title: Modifier l'approbation d'une inscription à un classe ✅
description: Route pour modifier l'approbation d'une inscription à une classe
---

Route pour modifier l'approbation d'une inscription à une classe.

- **URL**

  /api/shows/{showId}/classes/{classesId}/inscriptions/{inscriptionId}

- **Méthode:**

  `PATCH`

- **Paramètres:**

  **Requis:**

        Content-Type:  JSON

        `approved=[boolean]`<br>

- **Réponse de succès:**

  - **Code:** 200 <br />
    **Contenu:**
    ```json
    {
      "show_id": 1,
      "user_id": 1,
      "no_fei": "FEI123",
      "nb_stalls": 2,
      "nb_hay_bale": 5,
      "nb_chiving_bags": 3,
      "has_payed": true,
      "approved": true,
      "createdAt": "2024-02-15T22:26:12.298Z",
      "updatedAt": "2024-02-15T22:45:05.184Z",
      "class_id": 1
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

- **Code:** 404 NOT FOUND <br />
  **Contenu:**
  ```json
  { "message": "La ressource n’existe pas." }
  ```
