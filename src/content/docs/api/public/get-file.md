---
title: Obtenir un fichier dans le dossier public 🛑
description: Route pour obtenir un fichier
---

Route pour obtenir un fichier.

- **URL**

  /public/{nom du path du fichier sans ssrc/public/documents}

- **Méthode:**

  `GET`

- **Réponse de succès:**
  - **Code:** 200 <br />
    **Contenu:**
    ```json
    File
    ```

* **Réponse d'erreur:**

  * **Code:** 404 NOT FOUND <br />
    **Contenu:** 
    ```json
    { "message": "La ressource n’existe pas." }
    ```
 
