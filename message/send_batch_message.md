# Messages - Send Batch Message

Endpoint for sending Batch Message

## Resource

```
POST /message/send_batch_message
```

## Parameters


Name              	| Type   	| Description
:------------------|:----------	|:--------------------
login_hash			|string		|**[required]** <user hash key>
site_lang		  	|string	 	|**[required]** en
message | string |
msg_id  | int |
recipients  | int |
reply_message | int |
subject | string |
thread_id | int |



## Example

### Request
***

```curl
curl -X POST "http://staging-api.deplacementpeninsule.ca/api/message/send_batch_message?site_lang=en&login_hash=4fee9065a6c6365ddef03cc5102e67fe&message=&msg_id=&recipients=&reply_message=&subject=&thread_id="
```

### Response
***

**Status-Code:**

```json

```


### Error Responses
***
<!--No Login Hash
With Login Hash and others filled in
With Login Hash and no data filled in-->
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
