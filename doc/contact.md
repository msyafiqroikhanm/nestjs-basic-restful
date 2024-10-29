# Contact API Specs

## Create Contact

Endpoint : POST /api/contacts

Headers:

- authorization : token

Request Body :

```json
{
  "first_name": "roikhan",
  "last_name": "maulana",
  "email": "roikhan.maulana@gmail.com",
  "phone": "08123791827398"
}
```

Response Body (Success);

```json
{
  "data": {
    "id": 1,
    "first_name": "roikhan",
    "last_name": "maulana",
    "email": "roikhan.maulana@gmail.com",
    "phone": "08123791827398"
  }
}
```

Response Body (Failed);

```json
{
  "errors": "email already registered"
}
```

## Get Contact

Endpoint : GET /api/contacts/:contactId

Headers:

- authorization : token

Request Body :

```json
{
  "first_name": "roikhan",
  "last_name": "maulana",
  "email": "roikhan.maulana@gmail.com",
  "phone": "08123791827398"
}
```

Response Body (Success);

```json
{
  "data": {
    "id": 1,
    "first_name": "roikhan",
    "last_name": "maulana",
    "email": "roikhan.maulana@gmail.com",
    "phone": "08123791827398"
  }
}
```

## Update Contact

Endpoint : PUT /api/contacts/:contactId

Headers:

- authorization : token

Request Body :

```json
{
  "first_name": "roikhan",
  "last_name": "maulana",
  "email": "roikhan.maulana@gmail.com",
  "phone": "08123791827398"
}
```

Response Body (Success);

```json
{
  "data": {
    "id": 1,
    "first_name": "roikhan",
    "last_name": "maulana",
    "email": "roikhan.maulana@gmail.com",
    "phone": "08123791827398"
  }
}
```

## Remove Contact

Endpoint : DELETE /api/contacts/:contactId

Headers:

- authorization : token

Response Body (Success);

```json
{
  "data": true
}
```

## Search Contact

Endpoint : GET /api/contacts

Headers:

- authorization : token

Query Params :

- name : string, contact first name or contact last name, optional
- phone : string, contact phone, optional
- email : string, contact email, optional
- page : number, default 1
- size : number, default 10

Request Body :

```json
{
  "first_name": "roikhan",
  "last_name": "maulana",
  "email": "roikhan.maulana@gmail.com",
  "phone": "08123791827398"
}
```

Response Body (Success);

```json
{
  "data": [
    {
      "id": 1,
      "first_name": "roikhan",
      "last_name": "maulana",
      "email": "roikhan.maulana@gmail.com",
      "phone": "08123791827398"
    },
    {
      "id": 1,
      "first_name": "roikhan",
      "last_name": "maulana",
      "email": "roikhan.maulana@gmail.com",
      "phone": "08123791827398"
    }
  ],
  "paging": {
    "current_page": 1,
    "total_page": 10,
    "size": 10
  }
}
```
