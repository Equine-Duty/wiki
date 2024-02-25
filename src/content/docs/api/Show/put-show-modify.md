---
title: Modifier un show ✅
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
    `nb_total_place=[int]`<br>
    `nb_temp_stalls=[int]`<br>
    `nb_tack_stalls=[int]`<br>
    `nb_permanent_stalls=[int]`<br>
    `recognized_show=[boolean]`<br>
    `rules=[string]`<br>
    `start_date=[string]`<br>
    `end_date=[string]`<br>
    `inscription_end_date=[string]`<br>
    `inscription_end_late_date=[string]`<br>
    `inscription_start_date=[string]`<br>
    `asked_codes=[string]`<br>
    `is_vaccination_proof_required=[boolean]`<br>
    `is_coggins_proof_required=[boolean]`<br>
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


  * **Code:** 400 Bad Request <br />
    **Contenu:** 
    ```json
    { "errorMessage": ["Asked codes must be unique","Not enough permanent stalls", "Not enough tack stalls"
    , "Not enough temp stalls", "Not enough place",
    "End date cannot be before start date", "Start date cannot be before inscription end date",
     "Late inscription date cannot be before end date", "End date cannot be before start date",
      "The show inscription start date is in the past",] }
    ```
* **Code:** 400 Bad Request <br />
    **Contenu:** 
    ```json
    { "error": "There can only be one file named show_logo." }

* **Code:** 400 Bad Request <br />
    **Contenu:** 
    ```json
    { "error": "Inscription end date cannot be before inscription start date" }

* **Code:** 400 Bad Request <br />
    **Contenu:** 
    ```json
    { "error": "Late inscription date cannot be before inscription end date" }

* **Code:** 400 Bad Request <br />
    **Contenu:** 
    ```json
    { "error": "Start date cannot be before inscription end date or inscription end late date" }

* **Code:** 400 Bad Request <br />
    **Contenu:** 
    ```json
    { "error": "Not enough total place" }


* **Code:** 400 Bad Request <br />
    **Contenu:** 
    ```json
    { "error": "Not enough tack stalls" }


* **Code:** 400 Bad Request <br />
    **Contenu:** 
    ```json
    { "error": "Not enough permanent stalls" }


* **Code:** 400 Bad Request <br />
    **Contenu:** 
    ```json
    { "error": "Not enough temp stalls" }

  * **Code:** 401 UNAUTHORIZED <br />
    **Contenu:** 
    ```json
    { "message": "Unauthorized" }
    ```

  * **Code:** 403 FORBIDDEN <br />
    **Contenu:** 
    ```json
    { "message": "Forbidden" }
    ```

  * **Code:** 404 NOT FOUND <br />
    **Contenu:** 
    ```json
    { "error": "Show id not found" }
    ```
