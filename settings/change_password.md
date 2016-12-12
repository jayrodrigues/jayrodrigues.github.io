# Settings - Change Password

Endpoint to update the users Password in Settings.

## Resource

```
GET /settings/change_password
```

## Parameters


Name              	| Type   	| Description
:------------------|:----------	|:--------------------
login_hash			|string		|**[required]** <user hash key>
old_password  |string|
new_password |string|


## Example

### Request
***

```curl
curl -X GET "http://staging-api.deplacementpeninsule.ca/api/settings/change_password?login_hash=4fee9065a6c6365ddef03cc5102e67fe&old_password=pa55word09&new_password=pa55word09"
```

### Response
***

**Status-Code:** ```200 OK```

```json
{
  "message": "Your password has been successfully changed.",
  "status": true
}
```


### Error Responses
***

**Status-Code:** ```200 OK```


```json
{
  "message": "Your current password is incorrect.",
  "status": false
}
```
