# Offer Ride - Update Ride Price

Endpoint for Updating Ride Price - Step 2

## Resource

```
POST /ride/update_price
```

## Parameters


| URI Parameter | Type   | Required | Description |
|:--------------|:-------|:---------|:------------|
| login_hash    | string |       |             |
| site_lang     | string | yes      | en          |
| stopover[id]  | String      |          | |
| stopover[ride_id]  | String      |          | |
| stopover[value]  | String      |          | |
| stopover[id]  | String      |          | |
| stopover[ride_id]  | String      |          | |
| stopover[value]  | String      |          | |

## Example

### Request
***

```curl
curl -X POST "http://staging-api.deplacementpeninsule.ca/api/ride/update_price?login_hash=4fee9065a6c6365ddef03cc5102e67fe&site_lang=en&stopover[id]=&stopover[ride_id]=&stopover[value]=&stopover[id]=&stopover[ride_id]=&stopover[value]="
```

### Response
***

**Status-Code:** ```200 OK```

<!--only thing entered was the site_lang. NO ride was posted through steps 1-3-->
```json
{
  "message": "Price updated successfully.",
  "status": true
}
```


### Error Responses
***
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
