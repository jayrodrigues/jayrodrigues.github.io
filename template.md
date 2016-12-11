# Book a Ride

The Ride Request endpoint allows a ride to be requested.

## Resource

```
GET example/:id
```

## Authorization

OAuth 2.0 bearer token with the request scope.

## Parameters

Name              	| Type   	| Description
:------------------	|:----------|:--------------------
site_lang			|string		|**required** en / fr
first_name		  	|string	 	|**required**
last_name		  	|string	 	|**required**


### Optional Parameters
***

Name              | Type    | Description
:-----------------|:--------|:------------
user_id			  |integer	 |**required**
size			  |integer	 |**optional**, values: 25, 28, 30, 32, 50, 54, 56, 60, 64, 108, 128, 135, 256, 270, 512 and original
fallback		  |boolean	 |**optional**


## Example
Optional message

### Request
***

```curl
curl -v -u 1971800d4d82861d8f2c1651fea4d212:api_token \
    -H "Content-Type: application/json" \
    -d '{"client":{"name":"Very Big Company","wid":777}}' \
    -X POST https://www.toggl.com/api/v8/clients
```

### Response
***

**Status-Code:** ```200 OK```

```json
{
    "data": {
        "id":1239455,
        "wid":777,
        "name":"Very Big Company",
        "at":"2013-02-26T08:45:28+00:00"
    }
}
```


### Error Responses
***

**Status-Code:** ```200 OK```


```json
{
    "data": {
        "id":1239455,
        "wid":777,
        "name":"Very Big Company",
        "at":"2013-02-26T08:45:28+00:00",
        "notes": "Contact: John Jacob Jingleheimer Schmidt"
    }
}
```

