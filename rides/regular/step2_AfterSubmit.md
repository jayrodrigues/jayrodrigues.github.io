# Offer Ride - Regular Lift - Step 2

Endpoint for Step 2 of offering Regular Rides. After form submit

## Resource

```
POST /ride/offer_ride
```

## Parameters

| URI Parameter                   | Type     | Required | Description |
|:--------------------------------|:---------|:---------|:------------|
| site_lang     | string | Yes      | en          |
| login_hash    | string | Yes      |             |
| step    | string | Yes      |pricing             |
| key     | string | Yes      |The unique identifier hash key of the ride             |
| ride_data[auto_accept]        | Int   |          |             |
| ride_data[chatting]        | Int   |          |             |
| ride_data[children]        | Int |          |             |
| ride_data[comment]          | String      |          |             |
| ride_data[detour]            | Int | |                 
| ride_data[food]              | Int      |          |             |
| ride_data[handicapped] | Int |          |             |
| ride_data[luggage_per_seat] | String |          |             |
| ride_data[music]  | Int      |          |             |
| ride_data[pets]  | Int      |          |             |
| ride_data[process]  | Int      |          |just to identify form get submitted or not. |
| ride_data[ride_id]  | String |          
| ride_data[seats_offered]  | String |          
| ride_data[smoking] | Int   |          |             |
| ride_data[steps_completed] | String |          |             |
| ride_data[veh_id] | String |          |             |
| ride_data[women_only] | Int |          |             |

## Example

### Request
***

```curl
curl -X POST "http://staging-api.deplacementpeninsule.ca/api/ride/offer_ride?site_lang=en&login_hash=4fee9065a6c6365ddef03cc5102e67fe&step=pricing&key=dbbb405d08f10bda4cd3bac8b312a3dc&ride_data[auto_accept]%20=1&ride_data[chatting]=0&ride_data[children]=0&ride_data[comment]=&ride_data[detour]=0&ride_data[food]=1&ride_data[handicapped]=0&ride_data[luggage_per_seat]=3&ride_data[music]=0&ride_data[pets]=0&ride_data[process]=1&ride_data[ride_id]=18&ride_data[seats_offered]=5&ride_data[smoking]=0&ride_data[steps_completed]=2&ride_data[veh_id]=30&ride_data[women_only]=1"
```

### Response
***

**Status-Code:**

```

```


### Error Responses
***
<!--
- No data aside from Login Hash and Site Language
- With Data entered
-->
**Status-Code:** ```200 OK```


```json
{
  "message": "Please send valid data.",
  "status": ""
}
```

<!--No Login Hash-->
**Status-Code:** ```200 OK```


```json
{
  "message": "Please log in with us. Don't have an account sign up now!",
  "status": false
}
```

<!--No Site Language-->
**Status-Code:** ```404 Not Found```


```
<!DOCTYPE HTML PUBLIC "-//IETF//DTD HTML 2.0//EN">
<html><head>
<title>404 Not Found</title>
</head><body>
<h1>Not Found</h1>
<p>The requested URL /fr/api/message/unread was not found on this server.</p>
</body></html>
```
