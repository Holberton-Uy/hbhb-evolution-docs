# Amenity Endpoints:

- POST /amenities:
  Payload:
  ```json
  {
    "name": "Wi-Fi"
  }
  ```
  Response:
  ```json
  {
    "id": "UUID4",
    "name": "Wi-Fi",
    "created_at": "2023-05-02T10:30:00Z",
    "updated_at": "2023-05-02T10:30:00Z"
  }
  ```

- GET /amenities:
  Response:
  ```json
  [
    {
      "id": "UUID4",
      "name": "Wi-Fi",
      "created_at": "2023-05-02T10:30:00Z",
      "updated_at": "2023-05-02T10:30:00Z"
    },
    ...
  ]
  ```

- GET /amenities/{amenity_id}:
  Response:
  ```json
  {
    "id": "UUID4",
    "name": "Wi-Fi",
    "created_at": "2023-05-02T10:30:00Z",
    "updated_at": "2023-05-02T10:30:00Z"
  }
  ```

- PUT /amenities/{amenity_id}:
  Payload:
  ```json
  {
    "name": "High-Speed Wi-Fi"
  }
  ```
  Response:
  ```json
  {
    "id": "UUID4",
    "name": "High-Speed Wi-Fi",
    "created_at": "2023-05-02T10:30:00Z",
    "updated_at": "2023-05-02T11:30:00Z"
  }
  ```

  - DELETE  /amenities/{amenity_id}:
  Response:
  ```json
  {
    "id": "UUID4",
    "name": "High-Speed Wi-Fi",
    "created_at": "2023-05-02T10:30:00Z",
    "updated_at": "2023-05-02T11:30:00Z"
  }
  ```
