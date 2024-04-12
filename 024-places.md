5. Place Endpoints:

- POST /places:
  Payload:
  ```json
  {
    "name": "Cozy Apartment",
    "description": "A beautiful and cozy apartment in the city center.",
    "address": "123 Main St",
    "city_id": "UUID4",
    "latitude": 40.7128,
    "longitude": -74.0060,
    "host_id": "UUID4",
    "number_of_rooms": 2,
    "number_of_bathrooms": 1,
    "price_per_night": 150.00,
    "max_guests": 4,
    "amenity_ids": ["UUID4", "UUID5"]
  }
  ```
  Response:
  ```json
  {
    "id": "UUID4",
    "name": "Cozy Apartment",
    "description": "A beautiful and cozy apartment in the city center.",
    "address": "123 Main St",
    "city_id": "UUID4",
    "latitude": 40.7128,
    "longitude": -74.0060,
    "host_id": "UUID4",
    "number_of_rooms": 2,
    "number_of_bathrooms": 1,
    "price_per_night": 150.00,
    "max_guests": 4,
    "amenity_ids": ["UUID4", "UUID5"],
    "created_at": "2023-05-02T10:30:00Z",
    "updated_at": "2023-05-02T10:30:00Z"
  }
  ```

- GET /places:
  Response:
  ```json
  [
    {
      "id": "UUID4",
      "name": "Cozy Apartment",
      "description": "A beautiful and cozy apartment in the city center.",
      "address": "123 Main St",
      "city_id": "UUID4",
      "latitude": 40.7128,
      "longitude": -74.0060,
      "host_id": "UUID4",
      "number_of_rooms": 2,
      "number_of_bathrooms": 1,
      "price_per_night": 150.00,
      "max_guests": 4,
      "amenity_ids": ["UUID4", "UUID5"],
      "created_at": "2023-05-02T10:30:00Z",
      "updated_at": "2023-05-02T10:30:00Z"
    },
    ...
  ]
  ```

- GET /places/{place_id}:
  Response:
  ```json
  {
    "id": "UUID4",
    "name": "Cozy Apartment",
    "description": "A beautiful and cozy apartment in the city center.",
    "address": "123 Main St",
    "city_id": "UUID4",
    "latitude": 40.7128,
    "longitude": -74.0060,
    "host_id": "UUID4",
    "number_of_rooms": 2,
    "number_of_bathrooms": 1,
    "price_per_night": 150.00,
    "max_guests": 4,
    "amenity_ids": ["UUID4", "UUID5"],
    "created_at": "2023-05-02T10:30:00Z",
    "updated_at": "2023-05-02T10:30:00Z"
  }
  ```

- PUT /places/{place_id}:
  Payload:
  ```json
  {
    "name": "Updated Cozy Apartment",
    "description": "An updated description for the apartment.",
    "price_per_night": 175.00,
    "max_guests": 5
  }
  ```
  Response:
  ```json
  {
    "id": "UUID4",
    "name": "Updated Cozy Apartment",
    "description": "An updated description for the apartment.",
    "address": "123 Main St",
    "city_id": "UUID4",
    "latitude": 40.7128,
    "longitude": -74.0060,
    "host_id": "UUID4",
    "number_of_rooms": 2,
    "number_of_bathrooms": 1,
    "price_per_night": 175.00,
    "max_guests": 5,
    "amenity_ids": ["UUID4", "UUID5"],
    "created_at": "2023-05-02T10:30:00Z",
    "updated_at": "2023-05-02T11:30:00Z"
  }
  ```

  - DELETE /places/{place_id}:
  Response:
  ```json
  {
    "id": "UUID4",
    "name": "Updated Cozy Apartment",
    "description": "An updated description for the apartment.",
    "address": "123 Main St",
    "city_id": "UUID4",
    "latitude": 40.7128,
    "longitude": -74.0060,
    "host_id": "UUID4",
    "number_of_rooms": 2,
    "number_of_bathrooms": 1,
    "price_per_night": 175.00,
    "max_guests": 5,
    "amenity_ids": ["UUID4", "UUID5"],
    "created_at": "2023-05-02T10:30:00Z",
    "updated_at": "2023-05-02T11:30:00Z"
  }
  ```  
