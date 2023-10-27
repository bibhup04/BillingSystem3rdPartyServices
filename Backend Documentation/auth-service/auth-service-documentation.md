# Auth Service

**Microservice for authentication**

**Contact:** Bibhu (<bibhusunder.b@prodapt.com>)

**Version:** v0.0.1

[Link to this project](https://github.com/bibhup04/onestop/tree/main/auth-service)

**Server URL:** http://localhost:9898

## Tags

### Auth controller

Allow users to login and register.

## Paths

### /auth/token

- **POST**

  - **Tags:** Auth controller
  - **Summary:** Login user
  - **Description:** User can login by providing username and password in `authRequest`.
  - **Operation ID:** getToken

  **Request Body:**

  ```json
  {
    "username": "string",
    "password": "string"
  }
