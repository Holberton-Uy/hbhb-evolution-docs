# Country Endpoints

- GET /countries:
  Response:
  ```json
  [
    {
      "id": "UUID4",
      "name": "United States",
      "code": "US",
      "created_at": "2023-05-02T10:30:00Z",
      "updated_at": "2023-05-02T10:30:00Z"
    },
    ...
  ]
  ```

- GET /countries/{country_code}:
  Response:
  ```json
  {
    "id": "UUID4",
    "name": "United States",
    "code": "US",
    "created_at": "2023-05-02T10:30:00Z",
    "updated_at": "2023-05-02T10:30:00Z"
  }
  ```

- GET /countries/{country_code}/cities:
  Response:
  ```json
  [
    {
      "id": "UUID4",
      "name": "New York",
      "country_id": "UUID4",
      "created_at": "2023-05-02T10:30:00Z",
      "updated_at": "2023-05-02T10:30:00Z"
    },
    ...
  ]
  ```

# City Endpoints

- POST /cities:
  Payload:
  ```json
  {
    "name": "New York",
    "country_id": "UUID4"
  }
  ```
  Response:
  ```json
  {
    "id": "UUID4",
    "name": "New York",
    "country_id": "UUID4",
    "created_at": "2023-05-02T10:30:00Z",
    "updated_at": "2023-05-02T10:30:00Z"
  }
  ```

- GET /cities/{city_id}:
  Response:
  ```json
  {
    "id": "UUID4",
    "name": "New York",
    "country_id": "UUID4",
    "created_at": "2023-05-02T10:30:00Z",
    "updated_at": "2023-05-02T10:30:00Z"
  }
  ```

- PUT /cities/{city_id}:
  Payload:
  ```json
  {
    "name": "New York City"
  }
  ```
  Response:
  ```json
  {
    "id": "UUID4",
    "name": "New York City",
    "country_id": "UUID4",
    "created_at": "2023-05-02T10:30:00Z",
    "updated_at": "2023-05-02T11:30:00Z"
  }
  ```

  - DELETE /cities/{city_id}:
  Response:
  ```json
  {
    "id": "UUID4",
    "name": "New York City",
    "country_id": "UUID4",
    "created_at": "2023-05-02T10:30:00Z",
    "updated_at": "2023-05-02T11:30:00Z"
  }
  ```
