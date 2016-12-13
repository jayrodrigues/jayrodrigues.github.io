# Settings - Membership - Online

Endpoint for Settings Stripe payment after form submitted. Online

## Resource

```
GET /settings/stripe
```

## Parameters


Name              	| Type   	| Description
:------------------|:----------	|:--------------------
login_hash			|string		|**[required]** <user hash key>
site_lang |string |**[required]** en
amount | string |
expiry_date | date |
stripe_token | string |
stripe_data[status] | string |


## Example

### Request
***

```curl
curl -X GET "http://staging-api.deplacementpeninsule.ca/api/settings/stripe?login_hash=4fee9065a6c6365ddef03cc5102e67fe&site_lang=en&amount=&expiry_date=&stripe_token=&stripe_data[status]="
```

### Response
***

**Status-Code:** ```200 OK```

```json
{
  "message": "Registration payment finished successfully. Enjoy the Lift.",
  "status": true
}
```


### Error Responses
***
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
