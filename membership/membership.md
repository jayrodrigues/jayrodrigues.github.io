# Settings - Membership

Endpoint to used with Membership Page (For form data)

## Resource

```
GET /settings/membership
```

## Parameters


| URI Parameter | Type   | Required | Description     |
|:--------------|:-------|:---------|:----------------|
| login_hash    | string | yes      | <user hash key> |
| site_lang     | string | yes      | en              |

## Example

### Request
***

```curl
curl -X GET "http://staging-api.deplacementpeninsule.ca/api/settings/membership?login_hash=4fee9065a6c6365ddef03cc5102e67fe&site_lang=en"
```

### Response
***

**Status-Code:** ```200 OK```

```json
{
  "membership_data": {
    "cur_language": "en",
    "lang": "en",
    "already_requested": 0,
    "amount": "10",
    "currency_code": "CAD",
    "point_sales": [
      {
        "id": "1",
        "en": "Tracadie",
        "fr": "Tracadie",
        "address_en": "Centre l’Échange Inc., \n3485 rue Albert,\nNB E1X 1C9,\n506-393-7460",
        "address_fr": "Centre l’Échange Inc., \n3485 rue Albert,\nNB E1X 1C9,\n506-393-7460"
      },
      {
        "id": "2",
        "en": "Paquetville",
        "fr": "Paquetville",
        "address_en": "Fondation Communautaire de la,\nPéninsule acadienne,\n095-2 rue du Parc,\nNB E8R 1J1,\n506-764-3364,",
        "address_fr": "Fondation Communautaire de la,\nPéninsule acadienne,\n095-2 rue du Parc,\nNB E8R 1J1,\n506-764-3364,"
      },
      {
        "id": "3",
        "en": "Caraquet",
        "fr": "Caraquet",
        "address_en": "Déplacement Péninsule,\n22 boul. St-Pierre Est,\nsous-sol bureau B106,\nNB E1W 1B6,\n506-727-2012",
        "address_fr": "Déplacement Péninsule,\n22 boul. St-Pierre Est,\nsous-sol bureau B106,\nNB E1W 1B6,\n506-727-2012"
      },
      {
        "id": "4",
        "en": "Shippagan",
        "fr": "Shippagan",
        "address_en": "Université de Moncton,\nCampus de Shippagan, Local 121,\n218 Boulevard J.-D.-Gauthier,\nShippagan, NB E8S 1P6,\n506-336-3400 poste 3453",
        "address_fr": "Université de Moncton,\nCampus de Shippagan, Local 121,\n218 Boulevard J.-D.-Gauthier,\nShippagan, NB E8S 1P6,\n506-336-3400 poste 3453"
      },
      {
        "id": "5",
        "en": "Neguac",
        "fr": "Néguac",
        "address_en": "Unique Family Center Inc.,\n1279 Rue Principale,\nNéguac NB E9G 1T4,\n506-779-1900",
        "address_fr": "Centre familial Unique Inc.,\n1279 Rue Principale,\nNéguac, NB, E9G 1T4, \n506-779-1900"
      },
      {
        "id": "6",
        "en": "Lamèque",
        "fr": "Lamèque",
        "address_en": "Secours Amitié Inc.,\r\n83 Rue du Pêcheur,\r\nLamèque, NB, \r\nE8T 1J3,\r\n506-344-5791",
        "address_fr": "Secours Amitié Inc.,\r\n83 Rue du Pêcheur,\r\nLamèque, NB,\r\nE8T 1J3,\r\n506-344-5791"
      }
    ],
    "offices": [
      {
        "id": "1",
        "en": "Deplacement Peninsule office",
        "fr": "Bureau de Déplacement Péninsule",
        "address_en": "22 boul. Is St-Pierre,\nCaraquet NB E1W 1B6",
        "address_fr": "22 boul. St-Pierre Est,\nCaraquet NB E1W 1B6"
      }
    ],
    "reg_data": null,
    "reg_notify": 0,
    "reg_expired": 0
  },
  "status": true
}
```


### Error Responses
***
<!--No Login Hash-->
**Status-Code:** ```200 OK```


```json
{
  "message": "Please log in with us. Don't have an account sign up now!",
  "status": false
}
```

<!--No Site Language-->
**Status-Code:** ```404 Not Found```


```
<!DOCTYPE HTML PUBLIC "-//IETF//DTD HTML 2.0//EN">
<html><head>
<title>404 Not Found</title>
</head><body>
<h1>Not Found</h1>
<p>The requested URL /fr/api/message/unread was not found on this server.</p>
</body></html>
```
