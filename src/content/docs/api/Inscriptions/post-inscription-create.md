---
title: S'inscrire à un concours ✅
---

Route pour s'inscrire à un concours

* **URL**

  /api/shows/{showId}/classes/{classesId}/inscriptions

* **Méthode:**
  
  `POST`

* **Vaidation:**
  - On valide si la classe appartient au show,
  - On vérifie que tout les ids existent
  - On vérifie que les id des bundles sont uniques
  - On vérifie que le date est pas plus grande que la durée du show
  - On vérifie que tu ne mets pas plus grand que 0 pour le nombre de jours si la les stalls et les tacks stalls sont à 0
  - On vérifie que si tu mets plus grand que 0 que au moins un des deux (stalls ou tacks) est plus grand que 0
  - On vérifie que les inscriptions sont dans les dates d'inscriptions
  - On vérifie que le show est publié 
<br>

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
    `nb_days=[int]`<br>
    `Shows_Packages=[array {"id": 1, "count": 1}]`<br>
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
<br>
* **Réponse de succès:**
  
  * **Code:** 201 <br />
    **Contenu:** 
    ```json
      {
        "id": 5,
        "horse_id": 1,
        "rider_id": 1,
        "show_id": 1,
        "user_id": 2,
        "no_fei": null,
        "nb_stalls": 1,
        "nb_tack_stalls": 1,
        "nb_hay_bale": 1,
        "nb_chipping_bags": 1,
        "stall_type": "PERMANENT",
        "nb_days": 2,
        "total": 349,
        "has_payed": false,
        "invoice_number": null,
        "approved": false,
        "rider_entry_number": 5,
        "createdAt": "2024-02-27T01:08:42.716Z",
        "updatedAt": "2024-02-27T01:08:42.716Z",
        "class_id": 1
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