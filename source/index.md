---
title: Crave API Reference

language_tabs:
  - Elaboration

includes:
  - errors

search: true
---

# Introduction

Welcome to the Crave API! You can use our API to access Crave API endpoints.

# Authorization

```auth_token``` is required for protected resources access. To access protected resources,
make sure to include ```auth_token``` in HTTP ```Authorization``` field.

> HTTP token authentication is used:

```http
POST /api/endpoint HTTP/1.1
Host: localhost:3000
Authorization: this_is_token
```


<aside class="notice">
Authorization: this_is_token
</aside>

# Posts

## Request Post list for app's main page

### HTTP Request
GET /posts.json

>Sample HTTP Request

```http
GET /teachers/posts.json?start_id=26
```

### Query Parameter

Parameter | Type | Description
--------- | ------- | -----------
start_id(optional) | int | only retrieve posts before the start_id(excluding), without this parameter, newest 20 posts will be returned


### Return
Fail: 400 bad request
Success: A JSON data with format.

>Sample Return Data

```json
{
    "posts": [
        {
            "image": "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSU4StnpPOOh4t4roN5impIzctYo6DG_63UT5mGFvFbeYMQNUONRw",
            "dish_name": "Tomyam Soup",
            "review": "Yummy!",
            "created_at": "2015-08-27T06:18:03.862Z",
            "updated_at": "2015-08-27T06:18:03.862Z",
            "post_id": 1,
            "rating": 4.5,
            "poster": "qing",
            "phone_number": "021 84900876",
            "address": "Jl. Caman Raya, Pondok Gede, BekasiIndonesia",
            "restaurant_name": "Chicken's Fe",
            "cost": "Rp70.000 for two people (approx.)CashCards accepted",
            "crave": 4,
            "price": 20,
            "style": "Thai",
            "latitude": -6.2635,
            "longitude": 106.9455,
            "tags": [
                {
                    "name": "spicy"

                },

                {
                    "name": "sichuan"
                }
            
            ],
            "comments": [

                {

                    "poster": "qing",
                    "content": "I want to eat!"
                
                },

                {
                    "poster": "qing",
                    "content": "Disbanderino!"
                }
            ]
        }
    ]

}
```