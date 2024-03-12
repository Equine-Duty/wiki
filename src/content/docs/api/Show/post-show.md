---
title: Créer un show ✅
description: Route pour céer un show
---

* **URL**

  /api/shows

* **Méthode:**
  
  `POST`

* **Paramètres:**

  Content-Type: form-data

  **Requis:**
 
    `name=[string]`<br>
    `address_id=[int]`<br>
    `organizer_id=[int]`<br>
    `can_have_late_registration=[boolean]`<br>
    `nb_total_place=[int]`<br>
    `nb_free_place=[int]`<br>
    `nb_temp_stalls=[int]`<br>
    `nb_permanent_stalls=[int]`<br>
    `nb_tack_stalls=[int]`<br>
    `nb_free_temp_stalls=[int]`<br>
    `nb_free_permanent_stalls=[int]`<br>
    `nb_free_tack_stalls=[int]`<br>
    `hay=[int]`<br>
    `chiving=[int]`<br>
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
    `recognized_show=[boolean]`<br>
    `rules=[string]`<br>
    `start_date=[string]`<br>
    `inscription_start_date=[string]`<br>
    `inscription_end_date=[string]`<br>
    `inscription_end_late_date=[string]`<br>
    `end_date=[string]`<br>
    `asked_codes=[string,string,string,...]`<br>

  **Optionnel**<br>
    `show_logo=[.pdf|.png|.jpeg]`<br>
    `inscription_end_late_date=[string]`<br>
   
* **Réponse de succès:**
  
  * **Code:** 201 <br />
    **Contenu:** 
    ```json
    {
      "id": 1,
      "name": "<nom du concours>"
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
