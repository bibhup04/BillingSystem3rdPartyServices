# Auth service

Microservice for authentication

### Contact Information
- Name: Bibhu
- Email: [bibhusunder.b@prodapt.com](mailto:bibhusunder.b@prodapt.com)
- Version: v0.0.1

### Project Link
- [Github Link](https://github.com/bibhup04/onestop/tree/main/auth-service)

### Server Information
Generated server URL: `http://localhost:9898`

## Tags

### Auth controller
Allow users to login and register.

## Paths

### /auth/token
- Method: POST
- Summary: Login user
- Description: User can login by providing a username and password in authRequest.
- Operation ID: getToken

### /auth/register
- Method: POST
- Summary: Register user
- Description: User can register by providing user credentials.
- Operation ID: addNewUser

### /auth/userId
- Method: GET
- Operation ID: home

## Schemas

### AuthRequest
- username (string)
- password (string)

### TokenDTO
- token (string)

### UserCredential
- id (integer)
- name (string)
- email (string)
- phoneNo (string)
- password (string)
- role (string)
- status (string)
