---
title: S'inscrire à un concours ✅
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
    `nb_stalls=[int]`<br>
    `nb_tack_stalls=[int]`<br>
    `nb_hay_bale=[int]`<br> 
    `nb_chipping_bags=[int]`<br>
    `show_asked_codes=[object or null]`<br>

    **Exemple:**
    ```json
    {
        "horse_id": 1,
        "rider_id": 1,
        "nb_stalls": 45,
        "nb_tack_stalls: 1"
        "nb_hay_bale": 30,
        "nb_chipping_bags": 43,
        "show_asked_codes": {
            "quebec_equestre": "123456789",
            "no_montreal": "qwerty123",
        }
    }
    ```

* **Réponse de succès:**
  
  * **Code:** 201 <br />
    **Contenu:** 
    ```json
    {
        "id": 1,
        "horse_id": 1,
        "rider_id": 1,
        "show_id": 1,
        "user_id": 1,
        "no_fei": null,
        "nb_stalls": 45,
        "nb_tack_stalls": 1,
        "nb_hay_bale": 30,
        "nb_chipping_bags": 43,
        "stall_type": "PERMANENT",
        "has_payed": false,
        "approved": false,
        "createdAt": "2024-02-08T21:13:53.948Z",
        "updatedAt": "2024-02-08T21:13:53.948Z",
        "class_id": 1,
        "total": 515
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