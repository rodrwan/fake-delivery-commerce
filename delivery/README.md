# Fake Delivery API

## Routes

```
POST /create

Creates a new delivery with cart item.

POST /stock

Stock check if the given collection of products has available stock.

GET /products

Returns a collection of product.
```

---

### POST /create

#### Request

```json
{
  "order": "5ba20094-e375-4f24-8b93-61621624d9ef",
  "cart": [
    {
      "name": "item 1",
      "price": 1000,
      "volume": 10
    },
    {
      "name": "item 2",
      "price": 2000,
      "volume": 10
    },
    {
      "name": "item 3",
      "price": 3000,
      "volume": 10
    }
  ]
}
```

#### Response

```json
{
  "data": {
    "name_on_card": "rodrigo fuenzalida",
    "pan": "8930084170586437",
    "reference_id": "57248090",
    "exp_date": "12/19",
    "balance": 0,
    "created_at": "2018-07-09T04:19:53.673770784Z"
  }
}
```

### POST /load

#### Request

```json
{
  "reference_id": "57248090",
  "amount": 100
}
```

#### Response

```json
{
  "data": {
    "name_on_card": "rodrigo fuenzalida",
    "pan": "6615486781025574",
    "reference_id": "18891417",
    "exp_date": "12/20",
    "balance": 1000,
    "created_at": "2018-07-09T00:12:52.269230017-04:00"
  }
}
```

### GET /

#### Response

```json
{
  "data": [
    {
      "name_on_card": "rodrigo fuenzalida",
      "pan": "8930084170586437",
      "reference_id": "57248090",
      "exp_date": "12/19",
      "balance": 0,
      "created_at": "2018-07-09T04:19:53.673770784Z"
    }
  ]
}
```
