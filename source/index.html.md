---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
- json
toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>
  - <a href='https://github.com/lord/slate'>Documentation Powered by Slate</a>

includes:
  - errors

search: true
---

# Introduction

# Authentication

# User Sign Up

This endpoint registers the user

> On successful signup the returned JSON structure is like this:

```json
[
  {
    "status": "success",
    "message": "Successfully created.",
    "data": {
      "emailAddress": "johndoe123@yopmail.com",
      "username": "John Doe",
      "zipCode": null,
      "geoZipCode": null,
      "JSESSIONID": "DA1DB0BBD07360F0EBB7DC2D51E32E58.web01staging"
    }
  }
]
```

### HTTP Request

`POST http://stage.internal.shopwell.com/v2/user`

### Headers

| Header       | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

# User Login

This endpoint logins the user

### HTTP Request

`POST http://stage.internal.shopwell.com/v2/session`

> Login request body

```json
[
  {
    "email_address": "johndoe123@yopmail.com",
    "password": "Engintech123"
  }
]
```

> If valid credentials are entered, the resulting response would be:

```json
[
  {
      "status": "success",
      "message": "Successfully created.",
      "data":{
      "emailAddress": "johndoe123@yopmail.com",
      "username": "John Doe",
      "zipCode": null,
      "geoZipCode": null,
      "JSESSIONID": "DA1DB0BBD07360F0EBB7DC2D51E32E58.web01staging"
  }
]
```

### Headers

| Header       | Description      |
| ------------ | ---------------- |
| Content-Type | application/json |

# Product

## Get a specific product details

This endpoint retrieves the details of a specific product

### HTTP Request

`GET http://stage.internal.shopwell.com/v2/product?upc=<product upc>`

> Request a specific product e.g
> GET http://stage.internal.shopwell.com/v2/product?upc=3680020950

> Response

```json
[
  {
      "status": "success",
      "data":{
      "product_details":{
      "avoid_by_profiles":[],
      "brand_name": "Food Club",
      "comments": null,
      "current_list_ids": null,
      "fit_score": 44,
      "fit_score_label": "Medium match for you",
      "fit_score_type": "MEDIUM",
      "id": 18,
      "last_purchased": null,
      "matches_avoids":[],
      "matches_dont_wants":[],
      "matches_moderation":[],
      "matches_wants":[],
      "moderation_flag": false,
      "nutrition_labels":{"nutrition_percentages":{"Total Fat": 0, "Saturated Fat": 0, "Carbohydrate": 0.3333333333333333, "Cholesterol": 0,…},
      "onlineStores":[],
      "primary_store_id": -1,
      "product_description": "Black Peppercorn",
      "product_image": "http://prod.shopwell.com/product/3680020950_thumb.png",
      "product_image_full": "http://prod.shopwell.com/product/3680020950_full.jpg",
      "product_name": "Marinade Mix",
      "product_size": 1.12,
      "product_size_unit": "Oz",
      "rating": null,
      "rating_stats":{"likes": 0, "dislikes": 0},
      "show_additional_details": true,
      "stores":[],
      "top_preference": null,
      "top_preference_multiple": null,
      "upc": "3680020950"
      },
      "alternate_products":[{"bestforme_index": 0, "brand_name": "Sylvia's Restaurant", "current_list_ids": null, "fit_score": "83",…],
      "trade_up_mode": true
}
  }
]
```

### Url Parameters

| Parameter | Description               |
| --------- | ------------------------- |
| upc       | upc of a specific product |
