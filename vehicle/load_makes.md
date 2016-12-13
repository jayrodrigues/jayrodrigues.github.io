# Settings - Vehicle - Load Makes

Endpoint to load Vehicle Makes when adding/editing a Vehicle.

## Resource

```
GET /settings/load_makes
```

## Parameters


| URI Parameter | Type   | Required | Description     |
|:--------------|:-------|:---------|:----------------|
| login_hash    | string | yes      | <user hash key> |
| year          | string | yes      |                 |


## Example

### Request
***

```curl
curl -X GET "http://staging-api.deplacementpeninsule.ca/api/settings/load_makes?login_hash=4fee9065a6c6365ddef03cc5102e67fe&year=2015"
```

### Response
***

**Status-Code:** ```200 OK```

```json
{
  "makes": [
    {
      "value": "1",
      "label": "ACURA"
    },
    {
      "value": "2",
      "label": "ALFA ROMEO"
    },
    {
      "value": "48",
      "label": "ASTON MARTIN"
    },
    {
      "value": "3",
      "label": "AUDI"
    },
    {
      "value": "4",
      "label": "BENTLEY"
    },
    {
      "value": "5",
      "label": "BMW"
    },
    {
      "value": "6",
      "label": "BUICK"
    },
    {
      "value": "7",
      "label": "CADILLAC"
    },
    {
      "value": "8",
      "label": "CHEVROLET"
    },
    {
      "value": "9",
      "label": "CHRYSLER"
    },
    {
      "value": "10",
      "label": "DODGE"
    },
    {
      "value": "52",
      "label": "FIAT"
    },
    {
      "value": "13",
      "label": "FORD"
    },
    {
      "value": "15",
      "label": "GMC"
    },
    {
      "value": "16",
      "label": "HONDA"
    },
    {
      "value": "17",
      "label": "HYUNDAI"
    },
    {
      "value": "18",
      "label": "INFINITI"
    },
    {
      "value": "20",
      "label": "JAGUAR"
    },
    {
      "value": "21",
      "label": "JEEP"
    },
    {
      "value": "42",
      "label": "KIA"
    },
    {
      "value": "49",
      "label": "LAMBORGHINI"
    },
    {
      "value": "22",
      "label": "LAND ROVER"
    },
    {
      "value": "23",
      "label": "LEXUS"
    },
    {
      "value": "24",
      "label": "LINCOLN"
    },
    {
      "value": "43",
      "label": "MASERATI"
    },
    {
      "value": "25",
      "label": "MAZDA"
    },
    {
      "value": "26",
      "label": "MERCEDES-BENZ"
    },
    {
      "value": "44",
      "label": "MINI"
    },
    {
      "value": "45",
      "label": "MITSUBISHI"
    },
    {
      "value": "28",
      "label": "NISSAN"
    },
    {
      "value": "32",
      "label": "PORSCHE"
    },
    {
      "value": "53",
      "label": "RAM"
    },
    {
      "value": "33",
      "label": "ROLLS-ROYCE"
    },
    {
      "value": "51",
      "label": "SCION"
    },
    {
      "value": "46",
      "label": "SMART"
    },
    {
      "value": "36",
      "label": "SUBARU"
    },
    {
      "value": "38",
      "label": "TOYOTA"
    },
    {
      "value": "39",
      "label": "VOLKSWAGEN"
    },
    {
      "value": "40",
      "label": "VOLVO"
    }
  ],
  "status": true
}
```


### Error Responses
***

**Status-Code:** ```200 OK```


```json
{
  "message": "Please send valid data.",
  "status": false,
  "makes": []
}
```
