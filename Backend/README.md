# API Documentation: `/user/register`

## Endpoint Description
The `/user/register` endpoint is used to register a new user in the system. It accepts user details such as name, email, and password, validates the input, and creates a new user in the database.

## HTTP Method
`POST`

## Request Body
The request body should be a JSON object with the following structure:

```json
{
  "fullname": {
    "firstname": "string (min length: 3)",
    "lastname": "string (optional, min length: 3)"
  },
  "email": "string (valid email format)",
  "password": "string (min length: 6)"
}
```

### Validation Rules
- `fullname.firstname`: Must be at least 3 characters long.
- `fullname.lastname`: Optional, but if provided, must be at least 3 characters long.
- `email`: Must be a valid email address.
- `password`: Must be at least 6 characters long.

## Response
### Success Response
**Status Code:** `201 Created`

**Response Body:**
```json
{
  "token": "string (JWT token)",
  "user": {
    "_id": "string",
    "fullname": {
      "firstname": "string",
      "lastname": "string"
    },
    "email": "string"
  }
}
```

### Error Responses
1. **Validation Error**
   - **Status Code:** `400 Bad Request`
   - **Response Body:**
     ```json
     {
       "errors": [
         {
           "msg": "string (error message)",
           "param": "string (field name)",
           "location": "string (body)"
         }
       ]
     }
     ```

2. **Server Error**
   - **Status Code:** `500 Internal Server Error`
   - **Response Body:**
     ```json
     {
       "error": "string (error message)"
     }
     ```

## Example Request
### Request
```http
POST /user/register HTTP/1.1
Content-Type: application/json

{
  "fullname": {
    "firstname": "John",
    "lastname": "Doe"
  },
  "email": "john.doe@example.com",
  "password": "password123"
}
```
