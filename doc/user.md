# User API Specs

## Register User

Endpoint : POST /api/users
Request Body :

```json
{
  "username": "syafiq",
  "password": "rahasia",
  "name": "Syafiq"
}
```

Response Body (Success);

```json
{
  "data": {
    "username": "syafiq",
    "name": "Syafiq"
  }
}
```

Response Body (Failed);

```json
{
  "errors": "Username already registered"
}
```

## Login User

Endpoint : POST /api/users/login
Request Body :

```json
{
  "username": "syafiq",
  "password": "rahasia"
}
```

Response Body (Success);

```json
{
  "data": {
    "username": "syafiq",
    "name": "Syafiq",
    "token": "session_id_generated"
  }
}
```

Response Body (Failed);

```json
{
  "errors": "Username or password is wrong"
}
```

## Get User

Endpoint : GET /api/users/current
Headers:

- authorization : token(session_id_generated)

Response Body (Success);

```json
{
  "data": {
    "username": "syafiq",
    "name": "Syafiq"
  }
}
```

Response Body (Failed);

```json
{
  "errors": "Unauthorized"
}
```

## Update User

Endpoint : PATCH /api/users/current
Headers:

- authorization : token(session_id_generated)

Request Body :

```json
{
  "name": "syafiq", // optional
  "password": "rahasia" // optional
}
```

Response Body (Success);

```json
{
  "data": {
    "username": "syafiq",
    "name": "Syafiq",
    "token": "session_id_generated"
  }
}
```

Response Body (Failed);

```json
{
  "errors": "Username or password is wrong"
}
```

## Logout User

Endpoint : DELETE /api/users/current
Headers:

- authorization : token(session_id_generated)

Response Body (Success);

```json
{
  "data": true
}
```
