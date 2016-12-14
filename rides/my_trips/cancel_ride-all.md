# My Trips - Upcoming trip - Cancel All Rides

Endpoints for upcoming trip (cancel all rides)

## Resource

```
GET /my_trips/handle_action
```

## Parameters


| URI Parameter | Type   | Required | Description |
|:--------------|:-------|:---------|:------------|
| login_hash    | string | yes      |             |
| method     | string |yes       |cancel_ride             |
| params_data[ride_id]     | string |yes       | 2            |


## Example

### Request
***

```curl
curl -X GET "http://staging-api.deplacementpeninsule.ca/api/my_trips/handle_action?login_hash=4fee9065a6c6365ddef03cc5102e67fe&method=cancel_ride¶ms_data[ride_id]=2"
```

### Response
***

```json
{
  "status": true,
  "message": "Lift Cancelled Successfully"
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
