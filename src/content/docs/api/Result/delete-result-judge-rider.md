---
title: Supprime le résultat d'un juge à un rider ✅
description: Route pour supprimer le résultat d'un juge à un rider par leur id.
---

Route pour supprimer le résultat d'un juge à un rider par leur id.

- **URL**

  /api/shows/{showId}/results/tests/{testId}/riders/{riderId}/judges/{judgeId}

- **Méthode:**

  `DELETE`

- **Réponse de succès:**

  - **Code:** 200 OK <br>
  **Contenu:**
  ```json
  {
    "id": 9,
    "test_id": 1,
    "rider_id": 1,
    "horse_id": 1,
    "horse_name": "Thunder",
    "rider_name": "Jane Doe",
    "score": 99,
    "nb_errors": 2,
    "reason": "VET_OUT",
    "judge_id": 1,
    "rider_entry_number": 1,
    "createdAt": "2024-02-28T07:21:51.201Z",
    "updatedAt": "2024-02-28T07:21:51.201Z"
  }
  ```

- **Réponse d'erreur:**

  - **Code:** 204 No Content