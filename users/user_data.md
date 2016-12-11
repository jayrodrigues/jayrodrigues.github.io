# Forgot Password

Function to get the data of a particular user

## Resource

```
GET /users/user
```

## Parameters

Name              	| Type   	| Description
:------------------	|:----------|:--------------------
hash_key				|string		|**[required]**


## Example


### Request
***

```curl
curl -X GET "http://staging-api.deplacementpeninsule.ca/api/users/user?hash_key=4fee9065a6c6365ddef03cc5102e67fe"
```

### Response
***

**Status-Code:** ```200 OK```

```json
{
  "user_data": {
    "id": "351",
    "hash_key": "4fee9065a6c6365ddef03cc5102e67fe",
    "ip_address": "172.68.58.168",
    "username": "ji.mmyjanesone@gmail.com",
    "email": "ji.mmyjanesone@gmail.com",
    "suggested_email": "ji.mmyjanesone@gmail.com",
    "email_verified": "0",
    "email_public": "1",
    "remember_code": null,
    "created_on": "1481492452",
    "last_login": "1481497798",
    "active": "1",
    "title": "",
    "first_name": "Jimmy",
    "last_name": "Janesone",
    "gender": "1",
    "house_number": null,
    "street": null,
    "address_line": null,
    "city": null,
    "post_code": null,
    "country": "0",
    "province": "0",
    "profile_pic": "http://rsa.myprodesigns.net/assets/img/user-m.svg",
    "dob": "0000-00-00",
    "company": null,
    "occupation": null,
    "extra_email": "",
    "phone": "",
    "suggested_phone": "",
    "phone_rejected": "",
    "phone_updated_date": "0000-00-00 00:00:00",
    "phone_verified": "0",
    "phone_public": "1",
    "extra_phone": null,
    "mobile_number": null,
    "mobile_verified_date": null,
    "mobile_verified_session_id": "0",
    "smoker": "0",
    "language": "",
    "maritial_status": "0",
    "user_description": "",
    "facebook_connected": "0",
    "facebook_url": null,
    "twitter_url": null,
    "gplus_url": null,
    "linkedin_url": null,
    "avg_vote": "0",
    "vote_count": "0",
    "id_proof": "",
    "id_proof_expiry_date": "0000-00-00",
    "id_proof_expiry_notify": "0",
    "id_proof_verified_date": "0000-00-00 00:00:00",
    "id_proof_verified_session_id": "0",
    "id_proof_upload_date": "0000-00-00 00:00:00",
    "id_proof_submited_method": "0",
    "driver_license": "",
    "license_number": "",
    "id_reject_session": "0",
    "social_login": "0",
    "user_identifier": null,
    "trashed": "0",
    "automated_user": "0",
    "first_login": "1",
    "modified_date": "0000-00-00 00:00:00"
  },
  "status": true
}
```


### Error Responses
***

**Status-Code:** ```200 OK```


```json
{
  "message": "Please send valid data.",
  "status": false,
  "user_data": []
}
```
