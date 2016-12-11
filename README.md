# RSA API Documentation

This is the v1 version of the document.

***

## Endpoints

### Registration
- [**`GET`** /users/sign_up](/users/registration.md)


### Authentication

- [**`GET`** /users/login](/users/login.md)
- [**`GET`** /users/social_login](/users/social_login.md)
- [**`GET`** /users/forgot_password](/users/forgot_password.md)

### Profile
- [**`GET`** /users/profile]()
- [**`GET`** /users/lic_verify]()
- [**`GET`** /users/membership_verify]()
- [**`GET`** /users/user (data)]()
- [**`GET`** /users/user (image)]()

### Request Rides

- [**`GET /ride`**](/users/com)
- [**`GET`** /search/list]()
- [**`GET`** /ride/ride_detail]()
- [**`GET`** /ride/book_ride]()


### Offer Rides

- [**`POST`** /ride/offer_ride]()
- [**`POST`** /ride/update_price]()
- [**`GET`** /ride/offer_ride]()
- [**`POST`** /ride/update_price]()
- [**`POST`** /ride/update_price]()

### My Trips: Driver
- [**`GET`** /my_trips/handle_action](/users/com)
- [**`GET`** /my_trips/handle_action]() (method: driver)
- [**`GET`** /my_trips/handle_action]() (method: driver_past)
- [**`POST`** /my_trips/handle_action]() (method: edit_ride)
- [**`GET`** /my_trips/handle_action]() (method: cancel_ride)


### My Trips: Passenger
- [**`GET`** /my_trips/handle_action]() (method: passenger)
- [**`GET`** /my_trips/handle_action]() (method: passenger_past)
- [**`POST`** /my_trips/handle_action]() (cancel passenger)



### Settings

- **[```GET /settings```](/users/com)**
- [**`GET`** /settings/change_password]()
- [**`GET`** /settings/personal_info]()
- [**`GET`** /settings/authentication]()
- [**`GET`** /settings/preference]()


### Vehicle


- [**`GET`** /settings/load_makes]()
- [**`GET`** /settings/load_models]()
- [**`GET`** /settings/co2_emission]()
- [**`GET`** /settings/veh_delete]()
- [**`GET`** /settings/vehicle]()
- [**`GET`** /settings/manage_veh]()

### Messages

- [**`GET`** /message](/users/com)
- [**`GET`** /message/unread]()
- [**`GET`** /message/inbox]()
- [**`GET`** /message/detail]()
- [**`POST`** /message/send_batch_message]()

### Ratings

- [**`GET`** /ratings](/users/com)
- [**`POST`** /ratings/rating_pending]()
- [**`POST`** /ratings/rating_received]()
- [**`POST`** /ratings/rating_given]()
- [**`POST`** /ratings/ratings/rating_campanign]()


### Deprecated
- **`GET`** /settings/membership
- **`GET`** /settings/membership (Direct Payment via office)
- **`GET`** /settings/stripe