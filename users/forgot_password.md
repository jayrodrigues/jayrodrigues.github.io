# Forgot Password

Endpoint to use to reset the user's password.

## Resource

```
GET /users/forgot_password
```

## Parameters

| URI Parameter | Type   | Required | Description                  |
|:--------------|:-------|:---------|:-----------------------------|
| email         | string | yes      | User's primary Email address |


## Example


### Request
***

```curl
curl -X GET "http://staging-api.deplacementpeninsule.ca/api/users/forgot_password?email=ji.mmyjanesone@gmail.com"
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
