# Offer Ride - One-Off - Step 2

Endpoint for Step 2 of offering an One-Off ride. Before form submit : for from data

## Resource

```
POST /ride/offer_ride
```

## Parameters


| URI Parameter | Type   | Required | Description |
|:--------------|:-------|:---------|:------------|
| site_lang     | string | yes      | en          |
| login_hash    | string | yes      |             |
| step    | string | yes      |pricing             |
| key     | string | yes      |The unique identifier hash key of the ride             |


## Example

### Request
***

```curl
curl -X POST "http://staging-api.deplacementpeninsule.ca/api/ride/offer_ride?site_lang=en&login_hash=4fee9065a6c6365ddef03cc5102e67fe&step=pricing&key=8603b2ebec73ab2076331df40659b491"
```

### Response
***

**Status-Code:** ```200 OK```

```json

```


### Error Responses
***
<!--data aside from Login Hash and Site Language-->
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
  "message": "Please send valid data.",
  "status": ""
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
