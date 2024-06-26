Review Endpoints:

- POST /places/{place_id}/reviews:
  Payload:
  ```json
  {
    "user_id": "UUID5",
    "rating": 4,
    "comment": "Great place, but could be a bit cleaner."
  }
  ```
  Response:
  ```json
  {
    "id": "UUID6",
    "place_id": "UUID4",
    "user_id": "UUID5",
    "rating": 4,
    "comment": "Great place, but could be a bit cleaner.",
    "created_at": "2023-05-02T10:30:00Z",
    "updated_at": "2023-05-02T10:30:00Z"
  }
  ```

- GET /places/{place_id}/reviews:
  Response:
  ```json
  [
    {
      "id": "UUID6",
      "place_id": "UUID4",
      "user_id": "UUID5",
      "rating": 4,
      "comment": "Great place, but could be a bit cleaner.",
      "created_at": "2023-05-02T10:30:00Z",
      "updated_at": "2023-05-02T10:30:00Z"
    },
    ...
  ]
  ```
  
- GET /users/{user_id}/reviews:
  Response:
  ```json
  [
    {
      "id": "UUID6",
      "place_id": "UUID4",
      "user_id": "UUID5",
      "rating": 4,
      "comment": "Great place, but could be a bit cleaner.",
      "created_at": "2023-05-02T10:30:00Z",
      "updated_at": "2023-05-02T10:30:00Z"
    },
    ...
  ]
  ```

- GET /reviews/{review_id}:
  Response:
  ```json
  {
    "id": "UUID6",
    "place_id": "UUID4",
    "user_id": "UUID5",
    "rating": 4,
    "comment": "Great place, but could be a bit cleaner.",
    "created_at": "2023-05-02T10:30:00Z",
    "updated_at": "2023-05-02T10:30:00Z"
  }
  ```
  
- DELETE /reviews/{review_id}:
  Response:
  ```json
  {
    "id": "UUID6",
    "place_id": "UUID4",
    "user_id": "UUID5",
    "rating": 3,
    "comment": "Updated comment: The place was not as clean as expected.",
    "created_at": "2023-05-02T10:30:00Z",
    "updated_at": "2023-05-02T11:30:00Z"
  }
  ```
