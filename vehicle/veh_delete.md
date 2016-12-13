# Settings - Vehicle Delete

Endpoint to delete a Vehicle.

## Resource

```
GET /settings/veh_delete
```

## Parameters


| URI Parameter | Type   | Required                       | Description |
|:--------------|:-------|:-------------------------------|:------------|
| site_lang     | string | **[required]** en              |             |
| login_hash    | string | **[required]** <user hash key> |             |
| veh_id        | string |                                |             |
| file_name     | string | optional                       |             |


## Example

### Request
***

```curl
curl -X GET "http://staging-api.deplacementpeninsule.ca/api/settings/veh_delete?site_lang=en&login_hash=4fee9065a6c6365ddef03cc5102e67fe&veh_id=80&file_name="
```

### Response
***

**Status-Code:** ```200 OK```

```json
{
  "message": "Vehicle deleted successfully.",
  "status": true
}
```


### Error Responses
***

**Status-Code:** ```200 OK```

<!--No Login_hash-->
```json
{
  "message": "Please log in with us. Don't have an account sign up now!",
  "status": false
}
```

**Status-Code:** ```200 OK```

<!--No veh_id-->
```json
{
  "message": "Failed to delete vehicle, a Lift has been booked with this vehicle!",
  "status": false
}
```
