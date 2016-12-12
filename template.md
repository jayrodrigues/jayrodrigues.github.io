# Photo Resources

```
GET example/:id
```

## Description

***

## Requires authentication

    ***

## Parameters

name              | type    | notes
:-----------------|:--------|:------------
user_id|integer|**required**
size|integer|**optional**, values: 25, 28, 30, 32, 50, 54, 56, 60, 64, 108, 128, 135, 256, 270, 512 and original
fallback|boolean|**optional**

    ***

    ## Return format

    ***

    ## Errors

    ***

## Example
**Request**

```curl
curl -X GET "http://staging-api.deplacementpeninsule.ca/api/users/sign_up?site_lang=en&first_name=Jane&last_name=Foster&gender=2&email=janefoster111@gmail.com&password=pa55word09"```

**Response**

```json
{
  "message": "Your account has been confirmed.",
  "status": true,
  "user_hash": "e9dab8436a741c936cf9f2f7476782c0"
}```



            [photo stream]: https://github.com/500px/api-documentation/blob/master/basics/formats_and_terms.md#500px-photo-terms
            [OAuth]: https://github.com/500px/api-documentation/tree/master/authentication
            [full format]: https://github.com/500px/api-documentation/blob/master/basics/formats_and_terms.md#full-format
            [short format]: https://github.com/500px/api-documentation/blob/master/basics/formats_and_terms.md#short-format-1
            [category]: https://github.com/500px/api-documentation/blob/master/basics/formats_and_terms.md#categories
