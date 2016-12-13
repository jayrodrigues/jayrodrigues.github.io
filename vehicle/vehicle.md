# Settings - Vehicle

Endpoint to Get vehicle data.

## Resource

```
GET /settings/vehicle
```

## Parameters


| URI Parameter | Type   | Required | Description     |
|:--------------|:-------|:---------|:----------------|
| veh_id        | string |          |                 |
| login_hash    | string | yes      | <user hash key> |

(specify logged in user hash to get all the vehicles of a that user)


## Example

### Request
***

```curl
curl -X GET "http://staging-api.deplacementpeninsule.ca/api/settings/vehicle?veh_id=&login_hash=4fee9065a6c6365ddef03cc5102e67fe"
```

### Response
***

<!--No Vehicle Added-->
**Status-Code:** ```200 OK```

```json
{
  "message": "No Vehicles Found",
  "status": false,
  "veh_data": []
}
```

<!--When a vehicle is added-->
**Status-Code:** ```200 OK```
```json
{
  "veh_data": [
    {
      "id": "80",
      "hash_key": "393190b9b8e5fbab9897d15104670579",
      "user_id": "351",
      "maker": "0",
      "model": "0",
      "year_built": "0000",
      "veh_id": "0",
      "transmission": "0",
      "mileage": "0",
      "veh_body_type": "0",
      "vehicle_image": "",
      "number_plate": "-",
      "color": "",
      "ac": "0",
      "tyre_type": "0",
      "distance_driven_per_year": "0",
      "co2_output": "",
      "fuel_efficiency": "",
      "luggage_size": "0",
      "seats": "0",
      "comfort_level": "0",
      "bike_rack": "0",
      "ski_rack": "0",
      "created_date": "2016-12-12 02:44:32",
      "modified_date": "2016-12-12 02:44:32",
      "modified_session_id": "351",
      "make_name": null,
      "model_name": null,
      "body_type": null,
      "license_code": "",
      "license_number": ""
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
  "message": "Please log in with us. Don't have an account sign up now!",
  "status": false
}
```
