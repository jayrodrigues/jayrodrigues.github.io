# My Trips - Upcoming trip - Edit Ride - Form Submit

Endpoints for upcoming trip (edit ride - form submit)

## Resource

```
POST /my_trips/handle_action
```

## Parameters


| URI Parameter | Type   | Required | Description |
|:--------------|:-------|:---------|:------------|
| login_hash    | string | yes      |             |
| method     | string |yes       |edit_ride             |
| params_data[auto_accept]     | Int |      |          |
| params_data[comment]     | String |      |          |
| params_data[detour]     | Int |      |          |
| params_data[flexibility]     | datetime |      |          |
| params_data[luggage_per_seat]     | String |      |          |
| params_data[price[37]]    | String |      |          |
| params_data[price[38]]     | String |      |          |
| params_data[process]     | Int |      |just to identify form get submitted or not.          |
| params_data[process_key]     | Int |      |          |
| params_data[published]     | Int |      |          |
| params_data[ride_id]     | string |yes       |params_data is an array of values           |
| params_data[seats_offered]     | String |      |          |
| params_data[veh_id]   | String |      |          |



## Example

### Request
***

```curl
curl -X POST "http://staging-api.deplacementpeninsule.ca/api/my_trips/handle_action?login_hash=4fee9065a6c6365ddef03cc5102e67fe&method=edit_ride¶ms_data[auto_accept]=¶ms_data[comment]=¶ms_data[detour]=¶ms_data[flexibility]=¶ms_data[luggage_per_seat]=¶ms_data[price[37]]=¶ms_data[price[38]]=¶ms_data[process]=¶ms_data[process_key]=¶ms_data[published]=¶ms_data[ride_id]=¶ms_data[seats_offered]=¶ms_data[veh_id]="
```

### Response
***

```json

```


### Error Responses
***
**Status-Code:** ```404 Not Found```

```json
{
  "status": false,
  "error": "Unknown method"
}
```
