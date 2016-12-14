# My Trips - Upcoming trip - Edit Ride - Edit Form

Endpoints for upcoming trip (edit ride - edit form)

## Resource

```
GET /my_trips/handle_action
```

## Parameters


| URI Parameter | Type   | Required | Description |
|:--------------|:-------|:---------|:------------|
| login_hash    | string | yes      |             |
| method     | string |yes       |edit_ride             |
| params_data[ride_id]     | string |yes       |params_data is an array of values           |

## Example

### Request
***

```curl
curl -X GET "http://staging-api.deplacementpeninsule.ca/api/my_trips/handle_action?login_hash=4fee9065a6c6365ddef03cc5102e67fe&method=edit_ride¶ms_data[ride_id]=1"
```

### Response
***

<!--With Login Hash and Method-->
```json
{
  "message": "You are not allowed to add a lift.",
  "status": ""
}
```


### Error Responses
***
**Status-Code:** ```200 OK```

<!--
- No Method entered
- With Method driver_past entered
-->

```json
{
  "message": "Please send valid data.",
  "status": ""
}
```

<!--
- With Method and Hash, No params_data[ride_id]
-->
```json
{
  "message": "You are not allowed to add a lift.",
  "status": ""
}
```
