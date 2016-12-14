# My Trips - Upcoming trip - Driver

Endpoints for upcoming trip (driver)

## Resource

```
GET /my_trips/handle_action
```

## Parameters


| URI Parameter | Type   | Required | Description |
|:--------------|:-------|:---------|:------------|
| login_hash    | string | yes      |             |
| method     | string |yes       |driver             |

## Example

### Request
***

```curl
curl -X GET "http://staging-api.deplacementpeninsule.ca/api/my_trips/handle_action?login_hash=4fee9065a6c6365ddef03cc5102e67fe&method=driver"
```

### Response
***

<!--With Login Hash and Method-->
```json
{
  "trip_data": [],
  "status": false
}
```


### Error Responses
***
**Status-Code:** ```200 OK```

<!--
- No Method entered
- With Method driver entered
-->

```json
{
  "message": "Please send valid data.",
  "status": ""
}
```
