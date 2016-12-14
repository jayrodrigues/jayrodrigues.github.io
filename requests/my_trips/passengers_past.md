# My Trips - Upcoming trip - Past Passenger

Endpoints for upcoming trip (past passenger)

## Resource

```
GET /my_trips/handle_action
```

## Parameters


| URI Parameter | Type   | Required | Description |
|:--------------|:-------|:---------|:------------|
| login_hash    | string | yes      |             |
| method     | string |yes       |passenger_past             |

## Example

### Request
***

```curl
curl -X GET "http://staging-api.deplacementpeninsule.ca/api/my_trips/handle_action?login_hash=4fee9065a6c6365ddef03cc5102e67fe&method=passenger_past"
```

### Response
***

<!--With Login Hash and Method-->
```json
{
  "trip_data": "",
  "status": true
}
```


### Error Responses
***
**Status-Code:** ```200 OK```

<!--
- No Method entered
- With Method passenger_past entered
-->

```json
{
  "message": "Please send valid data.",
  "status": ""
}
```
