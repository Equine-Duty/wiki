---
title: S'inscrire à un concours
---

Route pour s'inscrire à un concours

* **URL**

  /api/shows/{showId}/classes/{classesId}/inscriptions

* **Méthode:**
  
  `POST`

* **Paramètres:**

    **Requis:**

        Content-Type:  JSON

        `horse_id=[int]`<br>
        `rider_id=[int]`<br>
        `no_fei=[string|null]`<br>
        `nb_stalls=[int]`<br>
        `nb_hay_bale=[int]`<br> 
        `nb_chippings_bags=[int]`<br>


* **Réponse de succès:**
  
  * **Code:** 201 <br />
    **Contenu:** 
    ```json
    {
        "id": 1,
        "class_id": 1,
        "horse_id": 1,
        "rider_id": 1,
        "show_id": 1,
        "user_id": 1,
        "no_fei": null,
        "nb_stalls": 45,
        "nb_hay_bale": 30,
        "nb_chippings_bags": 43,
        "has_payed": false,
        "approved": false,
        "createdAt": "2024-02-08T21:13:53.948Z",
        "updatedAt": "2024-02-08T21:13:53.948Z"
    }
    ```

* **Réponse d'erreur:**

* **Code:** 401 UNAUTHORIZED <br />
    **Contenu:** 
    ```json
    { "message": "Non authentifié." }
    ```

  * **Code:** 404 NOT FOUND <br />
    **Contenu:** 
    ```json
    { "message": "La ressource n’existe pas." }
    ```