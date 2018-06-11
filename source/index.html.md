---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
- json
- curl

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>
  - <a href='https://github.com/lord/slate'>Documentation Powered by Slate</a>

includes:
  - errors

search: true
---

# Introduction

# Authentication

## User Login

This endpoint logins the user

### HTTP Request

`POST http://stage.internal.shopwell.com/v2/session`

> Login request example

```curl
curl -d "email_address=johndoe123@yopmail.com&password=Engintech123"
http://stage.internal.shopwell.com/v2/session
```

> Login response example:

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

# User

Represents user details.

### User Attributes

* id (Number) : Unique identifier
* Username(string) :  User name
* Email Address(string) : Email id of the user
* Password(string): Password of the user



## Create

### User Sign Up

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

# Product

## Product Show/Detail

### Product Attributes


### Get  product details

This endpoint retrieves the product details based on its upc value

### HTTP Request

`GET http://stage.internal.shopwell.com/v2/product?upc=<product upc>`


> Example Product Request with upc value 3680020950

```curl
> GET http://stage.internal.shopwell.com/v2/product?upc=3680020950
```

> Example Response 

```json
[
  {
    "status": "success",
    "data": {
        "product_details": {
            "avoid_by_profiles": [
            ],
            "brand_name": "Food Club",
            "comments": null,
            "current_list_ids": null,
            "fit_score": 44,
            "fit_score_label": "Medium match for you",
            "fit_score_type": "MEDIUM",
            "id": 18,
            "last_purchased": null,
            "matches_avoids": [
            ],
            "matches_dont_wants": [
            ],
            "matches_moderation": [
            ],
            "matches_wants": [
            ],
            "moderation_flag": false,
            "nutrition_labels": {
                "nutrition_percentages": {
                    "Total Fat": 0,
                    "Saturated Fat": 0,
                    "Carbohydrate": 0.3333333333333333,
                    "Cholesterol": 0,
                    "Sodium": 17,
                    "Potassium": 0,
                    "Fiber": 0,
                    "Vitamin A": 0,
                    "Vitamin C": 0,
                    "Vitamin D": 0,
                    "Vitamin E": 0,
                    "Vitamin B6": 0,
                    "Vitamin B12": 0,
                    "Calcium": 0,
                    "Iron": 2,
                    "Thiamin": 0,
                    "Riboflavin": 0,
                    "Niacin": 0,
                    "Phosphorus": 0,
                    "Iodine": 0,
                    "Zinc": 0,
                    "Magnesium": 0,
                    "Copper": 0,
                    "Folic Acid": 0
                },
                "nutrition_quantities": {
                    "Fat": {
                        "total": 0,
                        "breakdown": {
                            "Saturated Fat": 0,
                            "Trans Fat": 0
                        },
                        "uom": "G"
                    },
                    "Carbs": {
                        "total": 1,
                        "breakdown": {
                            "Fiber": 0,
                            "Sugar": 0
                        },
                        "uom": "G"
                    },
                    "Protein": {
                        "total": 0,
                        "breakdown": null,
                        "uom": "G"
                    },
                    "Cholesterol": {
                        "total": 0,
                        "breakdown": null,
                        "uom": "Mg"
                    },
                    "Sodium": {
                        "total": 410,
                        "breakdown": null,
                        "uom": "Mg"
                    },
                    "Potassium": {
                        "total": 0,
                        "breakdown": null,
                        "uom": ""
                    },
                    "Vitamin A": {
                        "total": 0,
                        "breakdown": null,
                        "uom": ""
                    },
                    "Vitamin C": {
                        "total": 0,
                        "breakdown": null,
                        "uom": ""
                    },
                    "Vitamin D": {
                        "total": 0,
                        "breakdown": null,
                        "uom": ""
                    },
                    "Vitamin E": {
                        "total": 0,
                        "breakdown": null,
                        "uom": ""
                    },
                    "Vitamin B6": {
                        "total": 0,
                        "breakdown": null,
                        "uom": ""
                    },
                    "Vitamin B12": {
                        "total": 0,
                        "breakdown": null,
                        "uom": ""
                    },
                    "Calcium": {
                        "total": 0,
                        "breakdown": null,
                        "uom": ""
                    },
                    "Iron": {
                        "total": 0.36,
                        "breakdown": null,
                        "uom": "mg"
                    },
                    "Thiamin": {
                        "total": 0,
                        "breakdown": null,
                        "uom": ""
                    },
                    "Riboflavin": {
                        "total": 0,
                        "breakdown": null,
                        "uom": ""
                    },
                    "Niacin": {
                        "total": 0,
                        "breakdown": null,
                        "uom": ""
                    },
                    "Phosphorus": {
                        "total": 0,
                        "breakdown": null,
                        "uom": ""
                    },
                    "Iodine": {
                        "total": 0,
                        "breakdown": null,
                        "uom": ""
                    },
                    "Zinc": {
                        "total": 0,
                        "breakdown": null,
                        "uom": ""
                    },
                    "Magnesium": {
                        "total": 0,
                        "breakdown": null,
                        "uom": ""
                    },
                    "Copper": {
                        "total": 0,
                        "breakdown": null,
                        "uom": ""
                    },
                    "Folic Acid": {
                        "total": 0,
                        "breakdown": null,
                        "uom": ""
                    }
                },
                "Calories": {
                    "total": 0,
                    "breakdown": {
                        "Fat Calories": 0
                    },
                    "uom": ""
                },
                "serving": {
                    "servingSize": 3,
                    "servingSizeAmount": "",
                    "servingsPerContainer": 10
                }
            },
            "onlineStores": [
            ],
            "primary_store_id": -1,
            "product_description": "Black Peppercorn",
            "product_image": "http://prod.shopwell.com/product/3680020950_thumb.png",
            "product_image_full": "http://prod.shopwell.com/product/3680020950_full.jpg",
            "product_name": "Marinade Mix",
            "product_size": 1.12,
            "product_size_unit": "Oz",
            "rating": null,
            "rating_stats": {
                "likes": 0,
                "dislikes": 0
            },
            "show_additional_details": true,
            "stores": [
            ],
            "top_preference": null,
            "top_preference_multiple": null,
            "upc": "3680020950"
        },
        "alternate_products": [
            {
                "bestforme_index": 0,
                "brand_name": "Sylvia's Restaurant",
                "current_list_ids": null,
                "fit_score": "83",
                "fit_score_type": "HIGH",
                "id": 280687,
                "matches_avoids": false,
                "matches_dont_wants": false,
                "matches_wants": false,
                "nearme_index": 0,
                "onlineStores": [
                ],
                "primary_store_id": -1,
                "product_description": "14.5 Oz",
                "product_image": "http://media.shopwell.com/kp/3068492666_thumb.png",
                "product_name": "Mixed Greens",
                "product_size": 12,
                "product_size_unit": "Pk",
                "rating": null,
                "rating_stats": {
                    "likes": 1,
                    "dislikes": 1
                },
                "result_position": 1,
                "stores": null,
                "upc": "3068492666"
            },
            {
                "bestforme_index": 1,
                "brand_name": "Shotgun Willie's",
                "current_list_ids": null,
                "fit_score": "78",
                "fit_score_type": "HIGH",
                "id": 278434,
                "matches_avoids": false,
                "matches_dont_wants": false,
                "matches_wants": false,
                "nearme_index": 1,
                "onlineStores": [
                ],
                "primary_store_id": -1,
                "product_description": "Texas Chili 3.1 Oz",
                "product_image": "http://media.shopwell.com/kp/3068490147_thumb.png",
                "product_name": "Seasoning",
                "product_size": 24,
                "product_size_unit": "Pk",
                "rating": null,
                "rating_stats": {
                    "likes": 9,
                    "dislikes": 9
                },
                "result_position": 2,
                "stores": null,
                "upc": "3068490147"
            },
            {
                "bestforme_index": 2,
                "brand_name": "Jeff Foxworthy",
                "current_list_ids": null,
                "fit_score": "74",
                "fit_score_type": "HIGH",
                "id": 186172,
                "matches_avoids": false,
                "matches_dont_wants": false,
                "matches_wants": false,
                "nearme_index": 2,
                "onlineStores": [
                ],
                "primary_store_id": -1,
                "product_description": "",
                "product_image": "http://media.shopwell.com/gladson/00041149322011_thumb.png",
                "product_name": "Chili Kit",
                "product_size": 2.21,
                "product_size_unit": "oz",
                "rating": null,
                "rating_stats": {
                    "likes": 2,
                    "dislikes": 0
                },
                "result_position": 3,
                "stores": null,
                "upc": "4114932201"
            },
            {
                "bestforme_index": 3,
                "brand_name": "Bearitos",
                "current_list_ids": null,
                "fit_score": "74",
                "fit_score_type": "HIGH",
                "id": 186443,
                "matches_avoids": false,
                "matches_dont_wants": false,
                "matches_wants": false,
                "nearme_index": 3,
                "onlineStores": [
                ],
                "primary_store_id": -1,
                "product_description": "Chili",
                "product_image": "http://media.shopwell.com/gladson/00024335513004_thumb.png",
                "product_name": "Seasoning",
                "product_size": 1.6,
                "product_size_unit": "oz",
                "rating": null,
                "rating_stats": {
                    "likes": 0,
                    "dislikes": 0
                },
                "result_position": 4,
                "stores": null,
                "upc": "2433551300"
            },
            {
                "bestforme_index": 4,
                "brand_name": "Jeff Foxworthy",
                "current_list_ids": null,
                "fit_score": "73",
                "fit_score_type": "HIGH",
                "id": 186181,
                "matches_avoids": false,
                "matches_dont_wants": false,
                "matches_wants": false,
                "nearme_index": 4,
                "onlineStores": [
                ],
                "primary_store_id": -1,
                "product_description": "Cajun",
                "product_image": "http://media.shopwell.com/gladson/00041149322028_thumb.png",
                "product_name": "Chili Kit",
                "product_size": 1.76,
                "product_size_unit": "oz",
                "rating": null,
                "rating_stats": {
                    "likes": 0,
                    "dislikes": 0
                },
                "result_position": 5,
                "stores": null,
                "upc": "4114932202"
            },
            {
                "bestforme_index": 5,
                "brand_name": "Bear Creek",
                "current_list_ids": null,
                "fit_score": "71",
                "fit_score_type": "HIGH",
                "id": 276627,
                "matches_avoids": false,
                "matches_dont_wants": false,
                "matches_wants": false,
                "nearme_index": 5,
                "onlineStores": [
                ],
                "primary_store_id": -1,
                "product_description": "Darn Good",
                "product_image": "http://www.shopwell.com/images/shopwell_product_thumb.png",
                "product_name": "Chili Mix",
                "product_size": 6,
                "product_size_unit": "Pk",
                "rating": null,
                "rating_stats": {
                    "likes": 0,
                    "dislikes": 0
                },
                "result_position": 6,
                "stores": null,
                "upc": "3068487576"
            },
            {
                "bestforme_index": 6,
                "brand_name": "Brooks",
                "current_list_ids": null,
                "fit_score": "70",
                "fit_score_type": "HIGH",
                "id": 109078,
                "matches_avoids": false,
                "matches_dont_wants": false,
                "matches_wants": false,
                "nearme_index": 6,
                "onlineStores": [
                ],
                "primary_store_id": -1,
                "product_description": "Secret Chili, Mild",
                "product_image": "http://media.shopwell.com/gladson/00023000920857_thumb.png",
                "product_name": "Seasoning",
                "product_size": 1.25,
                "product_size_unit": "oz",
                "rating": null,
                "rating_stats": {
                    "likes": 1,
                    "dislikes": 0
                },
                "result_position": 7,
                "stores": null,
                "upc": "2300092085"
            }
        ],
        "trade_up_mode": true
    }
}

]
```

### Url Parameters

| Parameter | Description               |
| --------- | ------------------------- |
| upc       | upc of a specific product |
