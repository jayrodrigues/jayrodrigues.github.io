# Registration

The registration endpoint is used to register new users accounts in RSA. 

## Resource

```
GET /api/users/sign_up
```

## Parameters


Name              	| Type   	| Description
:------------------|:----------	|:--------------------
site_lang			|string		|**required** en / fr
first_name		  	|string	 	|**required**
last_name		  	|string	 	|**required**
gender			  	|int		|**optional** 0 = male / 1 = female 
email				|string		|**optional**
password			|string		|**optional**



## Example


### Request
***

```curl
curl -X GET http://staging-api.deplacementpeninsule.ca/api/users/sign_up?site_lang=en&first_name=Jane&last_name=Foster&gender=2&email=janefoster111@gmail.com&password=pa55word09
```

### Response
***

**Status-Code:** ```200 OK```

```json
{
  "message": "Your account has been confirmed.",
  "status": true,
  "user_hash": "e9dab8436a741c936cf9f2f7476782c0"
}
```


### Error Responses
***

**Status-Code:** ```401 Invalid Data```


```json
{
  "message": "Please provide valid data",
  "status": false,
  "user_hash": {}
}
```

***

**Status-Code:** ```402 Email Already Exists```


```json
{
  "message": "User with this email address already exists.",
  "status": false,
  "user_hash": []
}
```