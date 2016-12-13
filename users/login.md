# Login

The registration endpoint is used to register new users accounts in RSA.

## Resource

```
GET /api/users/login
```

## Parameters

| URI Parameter | Type   | Required | Description           |
|:--------------|:-------|:---------|:----------------------|
| username      | string | yes      | Base64-encoded string |
| password      | string | yes      | Base64-encoded string |


## Example

### Request
***

```
curl -X GET http://staging-api.deplacementpeninsule.ca/api/users/login?username=janefoster111@gmail.com&password=pa55word09
```

### Response
***

**Status-Code:** ```200 OK```

```json
{
  "message": "Logged In Successfully",
  "status": true,
  "user_hash": "0a17bf11e528b6a3181b642956b1be1d"
}
```


### Error Responses
***

**Status-Code:** ```200 Authorized```


```json
{
  "message": "Incorrect Login",
  "status": false,
  "user_hash": []
}
```
