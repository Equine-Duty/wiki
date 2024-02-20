---
title: Modifier un show ⛔
description: Route pour modifier un show.
---

* **URL**

  /api/shows/{showId}

* **Méthode:**
  
  `PUT`

* **Paramètres:**

  Content-Type: form-data


  **Requis pour show n'est pas publié:**

    `name=[string]`<br>
    `address_id=[int]`<br>
    `nb_total_place=[boolean]`<br>
    `nb_temp_stalls=[boolean]`<br>
    `nb_tack_stalls=[boolean]`<br>
    `nb_permanent_stalls=[boolean]`<br>
    `recognized_show=[int]`<br>
    `rules=[string]`<br>
    `start_date=[string]`<br>
    `end_date=[string]`<br>
    `inscription_end_date=[string]`<br>
    `inscription_end_late_date=[string]`<br>
    `inscription_start_date=[string]`<br>
    `asked_codes=[string]`<br>
    `is_vaccination_proof_required=[boolean]`<br>
    `is_coggins_proof_required=[boolean]`<br>
    `is_published=[boolean]`<br>
    `hay=[int]`<br>
    `shaving=[int]`<br>
    `temp_stall_per_day=[int]`<br>
    `permanent_stall_per_day=[int]`<br>
    `tack_stall_per_day=[int]`<br>
    `drug_test=[int]`<br>
    `administration=[int]`<br>
    `late_inscription=[int]`<br>
    `cancel_inscription=[int]`<br>
    `ground=[int]`<br>
    `paramedics=[int]`<br>
    `camper_ground_rental=[int]`<br>
    `show_logo=[.png|.jpeg]`<br>

  **Requis pour show publié:** </br>
    `nb_total_place=[int]`<br>
    `nb_temp_stalls=[int]`<br>
    `nb_tack_stalls=[int]`<br>
    `nb_permanent_stalls=[int]`<br>
    `rules=[string]`<br>
   
* **Réponse de succès:**
  
  * **Code:** 200 <br />
    **Contenu:** 
    ```json
    {
      "data": {
        "id": 1,
        "name": "<nom du concours>"
      }
    }
    ```

* **Réponse d'erreur:**

  * **Code:** 401 UNAUTHORIZED <br />
    **Contenu:** 
    ```json
    { "message": "Non authentifié." }
    ```

  * **Code:** 403 FORBIDDEN <br />
    **Contenu:** 
    ```json
    { "message": "Cette action n’est pas autorisée." }
    ```

  * **Code:** 404 NOT FOUND <br />
    **Contenu:** 
    ```json
    { "message": "La ressource n’existe pas." }
    ```
