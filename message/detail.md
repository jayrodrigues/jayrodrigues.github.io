# Messages - Detail page

Endpoint for getting the Message Detail Page

## Resource

```
GET /message/detail
```

## Parameters


Name              	| Type   	| Description
:------------------|:----------	|:--------------------
login_hash			|string		|**[required]** <user hash key>
site_lang		  	|string	 	|**[required]** en
thread_hash   |string |**[required]**

## Example

### Request
***

```curl
curl -X GET "http://staging-api.deplacementpeninsule.ca/api/message/detail?login_hash=4fee9065a6c6365ddef03cc5102e67fe&site_lang=en&thread_hash=1"
```

### Response
***

**Status-Code:** ```200 OK```

```json
{
  "message_data": {
    "cur_language": "en"
  },
  "status": true
}
```


### Error Responses
***
<!--No Thread Hash-->
**Status-Code:** ```200 OK```


```json
{
  "redirectUrl": "http://staging-api.deplacementpeninsule.ca/message/inbox",
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
