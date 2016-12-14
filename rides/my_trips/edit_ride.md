# My Trips - Upcoming trip - Edit Ride

Endpoints for upcoming trip (edit ride)

## Resource

```
GET /my_trips/handle_action
```

## Parameters


| URI Parameter | Type   | Required | Description |
|:--------------|:-------|:---------|:------------|
| login_hash    | string | yes      |             |
| method     | string |yes       |edit_ride             |


## Example

### Request
***

```curl
curl -X GET "http://staging-api.deplacementpeninsule.ca/api/my_trips/handle_action?login_hash=4fee9065a6c6365ddef03cc5102e67fe&method=edit_ride"
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
