# Rating Campaign

This endpoint is used after rating form submitted

## Resource

```
POST /ratings/rating_campanign
```

## Parameters


Name              	| Type   	| Description
:------------------|:----------	|:--------------------
login_hash			|string		|**[required]** <user hash key>
site_lang		  	|string	 	|**[required]** en
ride_hash   | string  | <ride hash key>
ride_trip   | int |
comment | string |
data_count | int |
passenger_id | int |
passenger_stars_<passenger_id>  | string | just to append passenger id with parameters
format
comments_<passenger_id>   | string | just to append passenger id with parameters
format
process   | int | 1 = Submitted 0 = Not Submitted

## Example

### Request
***

```curl
curl -X POST "http://staging-api.deplacementpeninsule.ca/api/ratings/rating_campanign?login_hash=4fee9065a6c6365ddef03cc5102e67fe&site_lang=en&ride_hash=&ride_trip=&comment=&data_count=&passenger_id=&passenger_stars_%3Cpassenger_id%3E=&comments_%3Cpassenger_id%3E%20=&process="
```

### Response
***

**Status-Code:**

```

```


### Error Responses
***
<!--
- No Login Hash
- With Login Hash and Site Lang
- With all fields entered
-->
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
