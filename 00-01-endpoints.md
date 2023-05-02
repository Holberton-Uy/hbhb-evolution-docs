1. User Endpoints:

- POST /users:
  Payload:
  ```json
  {
    "email": "john@example.com",
    "password": "password123",
    "first_name": "John",
    "last_name": "Doe"
  }
  ```
  Response:
  ```json
  {
    "id": "UUID4",
    "email": "john@example.com",
    "first_name": "John",
    "last_name": "Doe",
    "created_at": "2023-05-02T10:30:00Z",
    "updated_at": "2023-05-02T10:30:00Z"
  }
  ```

- GET /users/{user_id}:
  Response:
  ```json
  {
    "id": "UUID4",
    "email": "john@example.com",
    "first_name": "John",
    "last_name": "Doe",
    "created_at": "2023-05-02T10:30:00Z",
    "updated_at": "2023-05-02T10:30:00Z"
  }
  ```

- PUT /users/{user_id}:
  Payload:
  ```json
  {
    "first_name": "Johnathan",
    "last_name": "Doe"
  }
  ```
  Response:
  ```json
  {
    "id": "UUID4",
    "email": "john@example.com",
    "first_name": "Johnathan",
    "last_name": "Doe",
    "created_at": "2023-05-02T10:30:00Z",
    "updated_at": "2023-05-02T11:30:00Z"
  }
  ```

2. Country Endpoints:

- POST /countries:
  Payload:
  ```json
  {
    "name": "United States",
    "code": "US"
  }
  ```
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

- PUT /countries/{country_code}:
  Payload:
  ```json
  {
    "name": "United States of America"
  }
  ```
  Response:
  ```json
  {
    "id": "UUID4",
    "name": "United States of America",
    "code": "US",
    "created_at": "2023-05-02T10:30:00Z",
    "updated_at": "2023-05-02T11:30:00Z"
  }
  ```

- GET /countries


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

3. City Endpoints:

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

4. Amenity Endpoints:

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

6. Review Endpoints:

- POST /reviews:
  Payload:
  ```json
  {
    "place_id": "UUID4",
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

- GET /reviews:
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

- PUT /reviews/{review_id}:
  Payload:
  ```json
  {
    "rating": 3,
    "comment": "Updated comment: The place was not as clean as expected."
  }
  ```
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
7. User Endpoints:

- POST /users:
  Payload:
  ```json
  {
    "email": "john.doe@example.com",
    "password": "secure_password",
    "first_name": "John",
    "last_name": "Doe"
  }
  ```
  Response:
  ```json
  {
    "id": "UUID7",
    "email": "john.doe@example.com",
    "first_name": "John",
    "last_name": "Doe",
    "created_at": "2023-05-02T10:30:00Z",
    "updated_at": "2023-05-02T10:30:00Z"
  }
  ```

- GET /users:
  Response:
  ```json
  [
    {
      "id": "UUID7",
      "email": "john.doe@example.com",
      "first_name": "John",
      "last_name": "Doe",
      "created_at": "2023-05-02T10:30:00Z",
      "updated_at": "2023-05-02T10:30:00Z"
    },
    ...
  ]
  ```

- GET /users/{user_id}:
  Response:
  ```json
  {
    "id": "UUID7",
    "email": "john.doe@example.com",
    "first_name": "John",
    "last_name": "Doe",
    "created_at": "2023-05-02T10:30:00Z",
    "updated_at": "2023-05-02T10:30:00Z"
  }
  ```

- PUT /users/{user_id}:
  Payload:
  ```json
  {
    "email": "john.doe_updated@example.com",
    "first_name": "John",
    "last_name": "Doe"
  }
  ```
  Response:
  ```json
  {
    "id": "UUID7",
    "email": "john.doe_updated@example.com",
    "first_name": "John",
    "last_name": "Doe",
    "created_at": "2023-05-02T10:30:00Z",
    "updated_at": "2023-05-02T11:30:00Z"
  }
  ```
