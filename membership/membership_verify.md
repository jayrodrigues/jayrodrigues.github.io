# Settings - Membership Verify

Endpoint used to Verify an users Membership

## Resource

```
GET /users/membership_verify
```

## Parameters


Name              	| Type   	| Description
:------------------|:----------	|:--------------------
login_hash			|string		|**[required]** <user hash key>
site_lang |string |**[required]** en

## Example

### Request
***

```curl
curl -X GET "http://staging-api.deplacementpeninsule.ca/api/users/membership_verify?login_hash=4fee9065a6c6365ddef03cc5102e67fe&site_lang=en"
```

### Response
***

**Status-Code:** ```200 OK```

```json
{
  "status": "Please send valid data."
}
```


### Error Responses
***
<!--No Login Hash-->
**Status-Code:** ```200 OK```


```json
{
  "status": "Please send valid data."
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
