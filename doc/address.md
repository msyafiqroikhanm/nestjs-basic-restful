# Address API Specs

## Create Address

Endpoint : POST /api/contacts/:contactId/addresses

Headers:

- authorization : token

Request Body :

```json
{
  "street": "Jalan Cempaka Putih",
  "city": "Pulogadung",
  "province": "DKI Jakarta",
  "country": "Indonesia",
  "postal_code": "123122"
}
```

Response Body (Success);

```json
{
  "data": {
    "id": 1,
    "street": "Jalan Cempaka Putih",
    "city": "Pulogadung",
    "province": "DKI Jakarta",
    "country": "Indonesia",
    "postal_code": "123122"
  }
}
```

## Get Address

Endpoint : GET /api/contacts/:contactId/addresses/:addressId

Headers:

- authorization : token

Response Body (Success);

```json
{
  "data": {
    "id": 1,
    "street": "Jalan Cempaka Putih",
    "city": "Pulogadung",
    "province": "DKI Jakarta",
    "country": "Indonesia",
    "postal_code": "123122"
  }
}
```

## Update Address

Endpoint : PUT /api/contacts/:contactId/addresses/:addressId

Headers:

- authorization : token

Request Body :

```json
{
  "street": "Jalan Cempaka Putih",
  "city": "Pulogadung",
  "province": "DKI Jakarta",
  "country": "Indonesia",
  "postal_code": "123122"
}
```

Response Body (Success);

```json
{
  "data": {
    "id": 1,
    "street": "Jalan Cempaka Putih",
    "city": "Pulogadung",
    "province": "DKI Jakarta",
    "country": "Indonesia",
    "postal_code": "123122"
  }
}
```

## Remove Address

Endpoint : DELETE /api/contacts/:contactId/addresses/:addressId

Headers:

- authorization : token

Response Body (Success);

```json
{
  "data": true
}
```

## List Addresses

Endpoint : GET /api/contacts/:contactId/addresses

Headers:

- authorization : token

Response Body (Success);

```json
{
  "data": [
    {
      "id": 1,
      "street": "Jalan Cempaka Putih",
      "city": "Pulogadung",
      "province": "DKI Jakarta",
      "country": "Indonesia",
      "postal_code": "123122"
    },
    {
      "id": 1,
      "street": "Jalan Cempaka Putih",
      "city": "Pulogadung",
      "province": "DKI Jakarta",
      "country": "Indonesia",
      "postal_code": "123122"
    }
  ]
}
```
