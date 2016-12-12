# Settings - Personal Info

Endpoint to update the users Personal Info in Settings.

## Resource

```
GET /settings/personal_info
```

## Parameters


Name              	| Type   	| Description
:------------------|:----------	|:--------------------
login_hash			|string		|**[required]** <user hash key>
address_line[address1]		  	|string	 	|
address_line[address2]		  	|string	 	|
city		|string  |
dob		|date  |1990-02-06
email |string |
extra_email1 | string | optional
extra_email2 | string | optional
email_public | int | (1=Yes 2=No)
first_name | string | Jimmy
gender | int | (1 = Male 2 = Female)
language | string | English, french
comment |
first_name | string | Janesone
maritial_status | int |
occupation | string | optional
phone | string |
extra_phone1 | string | optional
extra_phone2 | string | optional
phone_public | int | (1 = Yes 0 = No)
smoker | int | (1 = Yes 0 = No)
user_description | string |

## Example

### Request
***

```curl
curl -X GET "http://staging-api.deplacementpeninsule.ca/api/settings/personal_info?login_hash=4fee9065a6c6365ddef03cc5102e67fe&address_line[address1]%20=&address_line[address2]%20=&city=Toronto&dob=1990-02-06&email=ji.mmyjanesone@gmail.com&extra_email1=&extra_email2=&email_public=1&first_name=Jimmy&gender=1&language=english&last_name=Janesone&maritial_status=0&occupation=Software%20%20Engineer&phone=1234567890&extra_phone1=&extra_phone2=&phone_public=1&smoker=0&user_description="
```

### Response
***

**Status-Code:** ```200 OK```

```json
{
  "message": "User data updated successfully",
  "status": true
}
```


### Error Responses
***

**Status-Code:** ```200 OK```


```json
{
  "msg": "This email id already exist. Please try with another one.",
  "status": false
}
```
