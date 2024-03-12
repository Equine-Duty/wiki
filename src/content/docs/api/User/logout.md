---
title: Logout ✅
description: Route pour déconnecter un user.
---

Route pour déconnecter un user.

* **URL**

  /api/auth/logout

* **Méthode:**
  
  `GET`

* **Cookie:**

  **Requis:**
  refresh_token

* **Réponse de succès:**
  
  * **Code:** 200 OK<br />
    **Contenu:** <br>
    `string => Logged out`

* **Réponse d'erreur:**

  * **Code:** 500 Internal Server Error
