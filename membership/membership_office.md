# Settings - Membership - office

Endpoint for Settings Stripe payment after form submitted. office

## Resource

```
GET /settings/membership
```

## Parameters


Name              	| Type   	| Description
:------------------|:----------	|:--------------------
login_hash			|string		|**[required]** <user hash key>
site_lang |string |**[required]** en
office | int  |
payment_method | int  |
process | int  | 1 = Submitted 0 = Not Submitted


## Example

### Request
***

```curl
curl -X GET "http://staging-api.deplacementpeninsule.ca/api/settings/membership?login_hash=4fee9065a6c6365ddef03cc5102e67fe&site_lang=en&office=1&payment_method=3&process=1"
```

### Response
***

**Status-Code:** ```200 OK```

```json
{
  "msg": "Your payment verification request has been given for verification successfully.",
  "status": true
}
```


### Error Responses
***
<!--No payment method-->
**Status-Code:** ```200 OK```

```json
{
  "msg": "Failed to send your payment verification request. Please try again later.",
  "status": false
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
