1. User Endpoints:


- GET /users:
  Response:
  ```json
  [
  	{
  		"id": "ABCD-0123456789-XYZ",
  		"email": "john@example.com",
  		"first_name": "John",
  		"last_name": "Doe",
  		"created_at": "2023-05-02T10:30:00+00:00",
  		"updated_at": "2023-05-02T10:30:00+00:00"
  	},
  	{
  		"id": "ABCD-9876543210-XYZ",
  		"email": "jane@example.com",
  		"first_name": "Jane",
  		"last_name": "Something",
  		"created_at": "2024-04-02T10:30:00+00:00",
  		"updated_at": "2024-04-11T14:49:32.800895"
  	}
  ]
  ```

- POST /users:
  Payload:
  ```json
  {
    "email": "john@example.com",
    "first_name": "John",
    "last_name": "Doe"
  }
  ```
  Response:
  ```json
  {
    "id": "908ec2b8-8c5c-47f4-bc97-09fd20c78198",
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
    "id": "908ec2b8-8c5c-47f4-bc97-09fd20c78198",
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
    "id": "908ec2b8-8c5c-47f4-bc97-09fd20c78198",
    "email": "john@example.com",
    "first_name": "Johnathan",
    "last_name": "Doe",
    "created_at": "2023-05-02T10:30:00Z",
    "updated_at": "2023-05-02T11:30:00Z"
  }
  ```
  
- DELETE /users/{user_id}:
  Response:
  ```json
  {
    "id": "908ec2b8-8c5c-47f4-bc97-09fd20c78198",
    "email": "john@example.com",
    "first_name": "Johnathan",
    "last_name": "Doe",
    "created_at": "2023-05-02T10:30:00Z",
    "updated_at": "2023-05-02T11:30:00Z"
  }
  ```
