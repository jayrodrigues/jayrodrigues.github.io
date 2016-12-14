# RSA API Documentation

This is the v1 version of the document.

***

## Endpoints

### Registration
- [**`GET`** /users/sign_up](/users/registration.md)


### Authentication

- [**`GET`** /users/login](/users/login.md)
- [**`GET`** /users/social_login](/users/social_login.md) **
- [**`GET`** /users/forgot_password](/users/forgot_password.md)

### Profile
- [**`GET`** /users/profile](/users/profile.md)
- [**`GET`** /users/lic_verify](/users/lic_verify.md)
- [**`GET`** /users/user (data)](/users/user_data.md)
- [**`GET`** /users/user (image)]

### Request Rides

- [**`GET`** /search/list]
- [**`GET`** /ride/ride_detail]
- [**`GET`** /ride/book_ride]



### Offer Rides: One-Off

- [**`POST`** /ride/offer_ride](/rides/one-off/step1.md)
- [**`POST`** /ride/update_price](rides/update_price.md)
- [**`GET`** /ride/offer_ride]
- [**`POST`** /ride/update_price]
- [**`POST`** /ride/update_price]

### Offer Rides: Regular

- [**`POST`** /ride/offer_ride](/rides/regular/step1.md)
- [**`POST`** /ride/update_price]
- [**`GET`** /ride/offer_ride]
- [**`POST`** /ride/update_price]
- [**`POST`** /ride/update_price]

### My Trips: Driver (rides)
- [**`GET`** /my_trips/handle_action]
- [**`GET`** /my_trips/handle_action] (method: driver)
- [**`GET`** /my_trips/handle_action] (method: driver_past)
- [**`POST`** /my_trips/handle_action] (method: edit_ride)
- [**`GET`** /my_trips/handle_action] (method: cancel_ride)


### My Trips: Passenger (requests)
- [**`GET`** /my_trips/handle_action] (method: passenger)
- [**`GET`** /my_trips/handle_action] (method: passenger_past)
- [**`POST`** /my_trips/handle_action] (cancel passenger)



### Settings

- **[```GET /settings```](/users/com)**
- [**`GET`** /settings/change_password](/settings/change_password.md)
- [**`GET`** /settings/personal_info](/settings/personal_info.md)
- [**`GET`** /settings/authentication]
- [**`GET`** /settings/preference](/settings/preference.md)


### Vehicle


- [**`GET`** /settings/load_makes](/settings/load_makes.md)
- [**`GET`** /settings/load_models](/settings/load_models.md)
- [**`GET`** /settings/co2_emission](/settings/co2_emission.md)
- [**`GET`** /settings/veh_delete](/settings/veh_delete.md)
- [**`GET`** /settings/vehicle](/settings/vehicle.md)
- [**`GET`** /settings/manage_veh](/settings/manage_veh.md)

### Messages

- [**`GET`** /message]
- [**`GET`** /message/unread](/message/unread.md)
- [**`GET`** /message/inbox](/message/inbox.md)
- [**`GET`** /message/detail](/message/detail.md)
- [**`POST`** /message/send_batch_message](/message/send_batch_message.md)

### Ratings

- [**`GET`** /ratings]
- [**`POST`** /ratings/rating_pending](/ratings/rating_pending.md)
- [**`POST`** /ratings/rating_received](/ratings/rating_received.md)
- [**`POST`** /ratings/rating_given](/ratings/rating_given.md)
- [**`POST`** /ratings/ratings/rating_campanign](/ratings/rating_campanign.md)
- [**`POST`** /ratings/ratings/rating_campanign](/ratings/rating_campanign_after.md)


### Deprecated
- [**`GET`** /settings/membership](/membership/membership.md)
- [**`GET`** /settings/membership (Direct Payment via office)](/membership/membership_office.md)
- [**`GET`** /settings/stripe](/membership/stripe.md)
- [**`GET`** /users/membership_verify](/membership/membership_verify.md)
