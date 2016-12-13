# Settings - Vehicle - CO2 Emission

Endpoint to calculate the Co2 Emission for the users vehicle.

## Resource

```
GET /settings/co2_emission
```

## Parameters


| URI Parameter | Type   | Required | Description     |
|:--------------|:-------|:---------|:----------------|
| site_lang     | string | yes      | en              |
| login_hash    | string | yes      | <user hash key> |
| year          | string |          |                 |
| make_id       | int    |          |                 |
| model_id      | int    |          |                 |
| distance      | int    |          |                 |
| transmission  | int    |          |                 |
| mileage       | int    |          |                 |


## Example

### Request
***

```curl
curl -X GET "http://staging-api.deplacementpeninsule.ca/api/settings/co2_emission?site_lang=en&login_hash=4fee9065a6c6365ddef03cc5102e67fe&year=2015&make_id=1&model_in=2735&distance=110&transmission=1&mileage=1"
```

### Response
***

**Status-Code:** ```200 OK```

```json
""
```


### Error Responses
***

**Status-Code:** ```200 OK```


```json
""
```
