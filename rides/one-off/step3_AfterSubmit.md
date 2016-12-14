# Offer Ride - One-Off - Step 3

Endpoint for Step 3 of offering an One-Off ride. After form submit

## Resource

```
POST /ride/offer_ride
```

## Parameters

| URI Parameter                   | Type     | Required | Description |
|:--------------------------------|:---------|:---------|:------------|
| site_lang     | string | Yes      | en          |
| login_hash    | string | Yes      |             |
| step    | string | Yes      |confirm             |
| key     | string | Yes      |The unique identifier hash key of the ride             |
| ride_data[process]  | Int      | Yes         |just to identify form get submitted or not. |
| ride_data[ride_id]  | String |Yes   | Id of the ride       

## Example

### Request
***

```curl
curl -X POST "http://staging-api.deplacementpeninsule.ca/api/ride/offer_ride?site_lang=en&login_hash=4fee9065a6c6365ddef03cc5102e67fe&step=pricing&key=dbbb405d08f10bda4cd3bac8b312a3dc&ride_data[process]=1&ride_data[ride_id]=18"
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
