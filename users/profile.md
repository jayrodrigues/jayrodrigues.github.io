# User Profile

This endpoint is used to retrieve how the user's profile information. This endpoint can also be used to retrieve how others view the profile based on the privacy setting.

## Resource

```
GET /api/users/profile
```

## Parameters


| URI Parameter  | Type   | Required | Description                                                                            |
|:---------------|:-------|:---------|:---------------------------------------------------------------------------------------|
| public_profile | int    | yes      | 0: Logged in user's profile view. 1: Other users view this user's profile information. |
| user_hash      | string | yes      |                                                                                        |



## Example


### Request
***

```curl
curl -X GET "http://staging-api.deplacementpeninsule.ca/api/users/profile?public_profile=0&user_hash=4fee9065a6c6365ddef03cc5102e67fe"
```

### Response
***

**Status-Code:** ```200 OK```

```json
{
  "user_data": {
    "cur_language": "fr",
    "public_view": "0",
    "lang": "fr",
    "user_hash": "4fee9065a6c6365ddef03cc5102e67fe",
    "user_data": {
      "id": "351",
      "hash_key": "4fee9065a6c6365ddef03cc5102e67fe",
      "app_domain": "1",
      "ip_address": "172.68.58.168",
      "username": "ji.mmyjanesone@gmail.com",
      "password": "$2y$08$m.xlBNDW9pibdSZ1juJV4OWtB8NsvvDkQImZX7k8wCk8Bao43cLtK",
      "salt": null,
      "email": "ji.mmyjanesone@gmail.com",
      "suggested_email": "ji.mmyjanesone@gmail.com",
      "activation_code": "7d4198d1ad862c3bbf60e7546eaff7a27bc7b7f0",
      "email_verified": "0",
      "email_public": "1",
      "forgotten_password_code": null,
      "forgotten_password_time": null,
      "remember_code": null,
      "created_on": "1481492452",
      "last_login": "1481492611",
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
      "modified_date": "0000-00-00 00:00:00",
      "unix_id_proof_expiry_date": null,
      "admin_approved": 0
    },
    "preference_data": {
      "id": "206",
      "hash_key": "a8493b00f0f5bce773c7e58241cf945e",
      "user_id": "351",
      "chatting": "0",
      "smoking": "0",
      "food": "0",
      "pets": "0",
      "music": "0",
      "women_only": "0",
      "handicapped": "0",
      "children": "0"
    },
    "veh_datas": "No Vehicles Found",
    "rating_datas": "No Ratings Found",
    "ride_offered": [],
    "rides_happens": false
  },
  "status": true
}
```


### Error Responses
***

**Status-Code:** ```200 OK```


```json
{
  "message": "Please provide valid datas",
  "status": false,
  "user_data": []
}
```
