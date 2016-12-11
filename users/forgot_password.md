# Forgot Password

Endpoint to use to reset the user's password. 

## Resource

```
GET /users/forgot_password
```

## Parameters

Name              	| Type   	| Description
:------------------	|:----------|:--------------------
email				|string		|**[required]** User's primary Email address


## Example
Optional message

### Request
***

```curl
curl -X GET "http://staging-api.deplacementpeninsule.ca/api/users/forgot_password?email=janefoster111@gmail.com"
```

### Response
***

**Status-Code:** ```200 OK```

```json
{
  "message": "An email has been sent with instructions to reset your password.",
  "status": true
}
```


### Error Responses
***

**Status-Code:** ```200 OK```


```json
{
  "message": "Unable to Reset Password.",
  "status": ""
}
```

