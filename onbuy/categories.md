# Categories

Category endpoints allow you to browse and view OnBuy's product category structure for proper product classification.

## Overview

OnBuy uses a hierarchical category system to organize products. When creating products or listings, you must select an appropriate category that has `can_list_in: true`.

**Category Types:**
- **Department Store** (type_id: 1): Top-level departments
- **Summary** (type_id: 2): Mid-level groupings  
- **Standard** (type_id: 3): Specific categories for listings

**Important:** Only categories with `can_list_in: true` can be used for product listings.

## Categories: Browse

**Method:** `GET`

**URL:** `{{host}}/categories?site_id=2001&limit=14&offset=8&filter[onbuy_category_id]=10677, 3007&filter[category_type_id]=2&filter[name]=car&filter[can_list_in]=1&filter[seller_approved_for_refurbished]=1&filter[search]=foo`

**Authentication:** Required

**Example Response:**
```json
{
    "results": [
        {
            "category_id": 1,
            "name": "Root",
            "category_tree": "",
            "category_type_id": 0,
            "category_type": null,
            "parent_id": 0,
            "lvl": 1,
            "product_code_required": true,
            "seller_approved_for_refurbished": true,
            "can_list_in": false,
            "commission_tier_id": 3,
            "avaliable_condition_slugs": [
                "new",
                "refurbished",
                "excellent",
                "verygood",
                "good",
                "average",
                "belowaverage"
            ]
        },
        {
            "category_id": 2144,
            "name": "Baby & Toddler",
            "category_tree": null,
            "category_type_id": 1,
            "category_type": "Department Store",
            "parent_id": 1,
            "lvl": 2,
            "product_code_required": true,
            "seller_approved_for_refurbished": true,
            "can_list_in": false,
            "commission_tier_id": 3,
            "google_category": {
                "id": 537,
                "tree": "Baby & Toddler",
                "name": "Baby & Toddler",
                "level": 1
            },
            "avaliable_condition_slugs": [
                "new",
                "refurbished",
                "excellent",
                "verygood",
                "good",
                "average",
                "belowaverage"
            ]
        },
        {
            "category_id": 2150,
            "name": "Car Seats & Accessories",
            "category_tree": "Baby & Toddler",
            "category_type_id": 3,
            "category_type": "Standard",
            "parent_id": 2144,
            "lvl": 3,
            "product_code_required": true,
            "seller_approved_for_refurbished": true,
            "can_list_in": false,
            "commission_tier_id": 3,
            "google_category": {
                "id": 547,
                "tree": "Baby & Toddler > Baby Transport > Baby & Toddler Car Seats",
                "name": "Baby & Toddler Car Seats",
                "level": 3
            },
            "avaliable_condition_slugs": [
                "new",
                "refurbished",
                "excellent",
                "verygood",
                "good",
                "average",
                "belowaverage"
            ]
        },
        {
            "category_id": 2152,
            "name": "Healthcare & Hygiene",
            "category_tree": "Baby & Toddler",
            "category_type_id": 3,
            "category_type": "Standard",
            "parent_id": 2144,
            "lvl": 3,
            "product_code_required": true,
            "seller_approved_for_refurbished": true,
            "can_list_in": false,
            "commission_tier_id": 3,
            "google_category": {
                "id": 5252,
                "tree": "Baby & Toddler > Baby Health",
                "name": "Baby Health",
                "level": 2
            },
            "avaliable_condition_slugs": [
                "new",
                "refurbished",
                "excellent",
                "verygood",
                "good",
                "average",
                "belowaverage"
            ]
        },
        {
            "category_id": 2155,
            "name": "Nursery",
            "category_tree": "Baby & Toddler",
            "category_type_id": 2,
            "category_type": "Summary",
            "parent_id": 2144,
            "lvl": 3,
            "product_code_required": true,
            "seller_approved_for_refurbished": true,
            "can_list_in": false,
            "commission_tier_id": 3,
            "google_category": {
                "id": 554,
                "tree": "Furniture > Baby & Toddler Furniture",
                "name": "Baby & Toddler Furniture",
                "level": 2
            },
            "avaliable_condition_slugs": [
                "new",
                "refurbished",
                "excellent",
                "verygood",
                "good",
                "average",
                "belowaverage"
            ]
        },
        {
            "category_id": 2156,
            "name": "Nursing & Feeding",
            "category_tree": "Baby & Toddler",
            "category_type_id": 3,
            "category_type": "Standard",
            "parent_id": 2144,
            "lvl": 3,
            "product_code_required": true,
            "seller_approved_for_refurbished": true,
            "can_list_in": false,
            "commission_tier_id": 3,
            "google_category": {
                "id": 561,
                "tree": "Baby & Toddler > Nursing & Feeding",
                "name": "Nursing & Feeding",
                "level": 2
            },
            "avaliable_condition_slugs": [
                "new",
                "refurbished",
                "excellent",
                "verygood",
                "good",
                "average",
                "belowaverage"
            ]
        },
        {
            "category_id": 2157,
            "name": "Toilet Training",
            "category_tree": "Baby & Toddler",
            "category_type_id": 3,
            "category_type": "Standard",
            "parent_id": 2144,
            "lvl": 3,
            "product_code_required": true,
            "seller_approved_for_refurbished": true,
            "can_list_in": false,
            "commission_tier_id": 3,
            "google_category": {
                "id": 6952,
                "tree": "Baby & Toddler > Potty Training",
                "name": "Potty Training",
                "level": 2
            },
            "avaliable_condition_slugs": [
                "new",
                "refurbished",
                "excellent",
                "verygood",
                "good",
                "average",
                "belowaverage"
            ]
        },
        {
            "category_id": 2158,
            "name": "Pushchairs, Prams & Accessories",
            "category_tree": "Baby & Toddler",
            "category_type_id": 3,
            "category_type": "Standard",
            "parent_id": 2144,
            "lvl": 3,
            "product_code_required": true,
            "seller_approved_for_refurbished": true,
            "can_list_in": false,
            "commission_tier_id": 3,
            "google_category": {
                "id": 568,
                "tree": "Baby & Toddler > Baby Transport > Pushchairs & Prams",
                "name": "Pushchairs & Prams",
                "level": 3
            },
            "avaliable_condition_slugs": [
                "new",
                "refurbished",
                "excellent",
                "verygood",
                "good",
                "average",
                "belowaverage"
            ]
        },
        {
            "category_id": 2159,
            "name": "Safety Equipment",
            "category_tree": "Baby & Toddler",
            "category_type_id": 3,
            "category_type": "Standard",
            "parent_id": 2144,
            "lvl": 3,
            "product_code_required": true,
            "seller_approved_for_refurbished": true,
            "can_list_in": false,
            "commission_tier_id": 3,
            "google_category": {
                "id": 540,
                "tree": "Baby & Toddler > Baby Safety",
                "name": "Baby Safety",
                "level": 2
            },
            "avaliable_condition_slugs": [
                "new",
                "refurbished",
                "excellent",
                "verygood",
                "good",
                "average",
                "belowaverage"
            ]
        },
        {
            "category_id": 2161,
            "name": "Home, Garden & Pets",
            "category_tree": null,
            "category_type_id": 1,
            "category_type": "Department Store",
            "parent_id": 1,
            "lvl": 2,
            "product_code_required": true,
            "seller_approved_for_refurbished": true,
            "can_list_in": false,
            "commission_tier_id": 3,
            "google_category": {
                "id": 536,
                "tree": "Home & Garden",
                "name": "Home & Garden",
                "level": 1
            },
            "avaliable_condition_slugs": [
                "new",
                "refurbished",
                "excellent",
                "verygood",
                "good",
                "average",
                "belowaverage"
            ]
        },
        {
            "category_id": 2162,
            "name": "Swimming Pools & Hot Tubs",
            "category_tree": "Home, Garden & Pets",
            "category_type_id": 2,
            "category_type": "Summary",
            "parent_id": 2161,
            "lvl": 3,
            "product_code_required": true,
            "seller_approved_for_refurbished": true,
            "can_list_in": false,
            "commission_tier_id": 3,
            "google_category": {
                "id": 2810,
                "tree": "Home & Garden > Pool & Spa > Swimming Pools",
                "name": "Swimming Pools",
                "level": 3
            },
            "avaliable_condition_slugs": [
                "new",
                "refurbished",
                "excellent",
                "verygood",
                "good",
                "average",
                "belowaverage"
            ]
        },
        {
            "category_id": 2163,
            "name": "Water Testing & Chemicals",
            "category_tree": "Home, Garden & Pets > Swimming Pools & Hot Tubs",
            "category_type_id": 3,
            "category_type": "Standard",
            "parent_id": 2162,
            "lvl": 4,
            "product_code_required": true,
            "seller_approved_for_refurbished": true,
            "can_list_in": false,
            "commission_tier_id": 3,
            "google_category": {
                "id": 3017,
                "tree": "Home & Garden > Pool & Spa > Pool & Spa Accessories > Pool Cleaners & Chemicals",
                "name": "Pool Cleaners & Chemicals",
                "level": 4
            },
            "avaliable_condition_slugs": [
                "new",
                "refurbished",
                "excellent",
                "verygood",
                "good",
                "average",
                "belowaverage"
            ]
        },
        {
            "category_id": 2164,
            "name": "Toys & Games",
            "category_tree": null,
            "category_type_id": 1,
            "category_type": "Department Store",
            "parent_id": 1,
            "lvl": 2,
            "product_code_required": true,
            "seller_approved_for_refurbished": true,
            "can_list_in": false,
            "commission_tier_id": 3,
            "google_category": {
                "id": 1239,
                "tree": "Toys & Games",
                "name": "Toys & Games",
                "level": 1
            },
            "avaliable_condition_slugs": [
                "new",
                "refurbished",
                "excellent",
                "verygood",
                "good",
                "average",
                "belowaverage"
            ]
        },
        {
            "category_id": 2165,
            "name": "Outdoor Toys & Games",
            "category_tree": "Toys & Games",
            "category_type_id": 3,
            "category_type": "Standard",
            "parent_id": 2164,
            "lvl": 3,
            "product_code_required": true,
            "seller_approved_for_refurbished": true,
            "can_list_in": false,
            "commission_tier_id": 3,
            "google_category": {
                "id": 2672,
                "tree": "Home & Garden > Pool & Spa > Pool & Spa Accessories > Pool Toys",
                "name": "Pool Toys",
                "level": 4
            },
            "avaliable_condition_slugs": [
                "new",
                "refurbished",
                "excellent",
                "verygood",
                "good",
                "average",
                "belowaverage"
            ]
        },
        {
            "category_id": 2166,
            "name": "Garden Games & Activities",
            "category_tree": "Toys & Games > Outdoor Toys & Games",
            "category_type_id": 3,
            "category_type": "Standard",
            "parent_id": 2165,
            "lvl": 4,
            "product_code_required": true,
            "seller_approved_for_refurbished": true,
            "can_list_in": true,
            "commission_tier_id": 3,
            "google_category": {
                "id": 499846,
                "tree": "Sporting Goods > Outdoor Recreation > Outdoor Games",
                "name": "Outdoor Games",
                "level": 3
            },
            "avaliable_condition_slugs": [
                "new",
                "refurbished",
                "excellent",
                "verygood",
                "good",
                "average",
                "belowaverage"
            ]
        },
        {
            "category_id": 2168,
            "name": "Trampolines & Bouncy Castles",
            "category_tree": "Toys & Games > Outdoor Toys & Games",
            "category_type_id": 3,
            "category_type": "Standard",
            "parent_id": 2165,
            "lvl": 4,
            "product_code_required": true,
            "seller_approved_for_refurbished": true,
            "can_list_in": true,
            "commission_tier_id": 3,
            "google_category": {
                "id": 1738,
                "tree": "Toys & Games > Outdoor Play Equipment > Trampolines",
                "name": "Trampolines",
                "level": 3
            },
            "avaliable_condition_slugs": [
                "new",
                "refurbished",
                "excellent",
                "verygood",
                "good",
                "average",
                "belowaverage"
            ]
        },
        {
            "category_id": 2169,
            "name": "Play Centres, Swings & Slides",
            "category_tree": "Toys & Games > Outdoor Toys & Games",
            "category_type_id": 3,
            "category_type": "Standard",
            "parent_id": 2165,
            "lvl": 4,
            "product_code_required": true,
            "seller_approved_for_refurbished": true,
            "can_list_in": true,
            "commission_tier_id": 3,
            "google_category": {
                "id": 1249,
                "tree": "Toys & Games > Outdoor Play Equipment",
                "name": "Outdoor Play Equipment",
                "level": 2
            },
            "avaliable_condition_slugs": [
                "new",
                "refurbished",
                "excellent",
                "verygood",
                "good",
                "average",
                "belowaverage"
            ]
        },
        {
            "category_id": 2170,
            "name": "Playhouses & Tents",
            "category_tree": "Toys & Games > Outdoor Toys & Games",
            "category_type_id": 3,
            "category_type": "Standard",
            "parent_id": 2165,
            "lvl": 4,
            "product_code_required": true,
            "seller_approved_for_refurbished": true,
            "can_list_in": true,
            "commission_tier_id": 3,
            "google_category": {
                "id": 1249,
                "tree": "Toys & Games > Outdoor Play Equipment",
                "name": "Outdoor Play Equipment",
                "level": 2
            },
            "avaliable_condition_slugs": [
                "new",
                "refurbished",
                "excellent",
                "verygood",
                "good",
                "average",
                "belowaverage"
            ]
        },
        {
            "category_id": 2171,
            "name": "Sand & Water Toys",
            "category_tree": "Toys & Games > Outdoor Toys & Games",
            "category_type_id": 3,
            "category_type": "Standard",
            "parent_id": 2165,
            "lvl": 4,
            "product_code_required": true,
            "seller_approved_for_refurbished": true,
            "can_list_in": false,
            "commission_tier_id": 3,
            "google_category": {
                "id": 1249,
                "tree": "Toys & Games > Outdoor Play Equipment",
                "name": "Outdoor Play Equipment",
                "level": 2
            },
            "avaliable_condition_slugs": [
                "new",
                "refurbished",
                "excellent",
                "verygood",
                "good",
                "average",
                "belowaverage"
            ]
        },
        {
            "category_id": 2172,
            "name": "Paddling Pools",
            "category_tree": "Toys & Games > Outdoor Toys & Games > Sand & Water Toys",
            "category_type_id": 3,
            "category_type": "Standard",
            "parent_id": 2171,
            "lvl": 5,
            "product_code_required": true,
            "seller_approved_for_refurbished": true,
            "can_list_in": true,
            "commission_tier_id": 3,
            "google_category": {
                "id": 2810,
                "tree": "Home & Garden > Pool & Spa > Swimming Pools",
                "name": "Swimming Pools",
                "level": 3
            },
            "avaliable_condition_slugs": [
                "new",
                "refurbished",
                "excellent",
                "verygood",
                "good",
                "average",
                "belowaverage"
            ]
        }
    ],
    "metadata": {
        "limit": 20,
        "offset": 0,
        "total_rows": 6938
    }
}
```

---

## Categories: View

**Method:** `GET`

**URL:** `{{host}}/categories/{{category_id}}?site_id=2001`

**Authentication:** Required

**Example Response:**
```json
{
    "results": {
        "category_id": 3428,
        "name": "Men's Sweatshirts &  Hoodies",
        "category_tree": "Clothing, Shoes & Accessories > Men's Clothing > Men's Knits & Sweaters",
        "category_type_id": 3,
        "category_type": "Standard",
        "parent_id": 34259,
        "lvl": 5,
        "restricted_listing": 0,
        "product_code_required": 1,
        "can_list_in": 1,
        "google_category": {
            "id": 212,
            "tree": "Clothing & Accessories > Clothing > Shirts & Tops",
            "name": "Shirts & Tops",
            "level": 3
        },
        "avaliable_condition_slugs": [
            "new"
        ],
        "commission_tier_id": "98ce396a-9348-44fe-9c55-fd8943768562",
        "features": [
            {
                "feature_id": 1,
                "name": "Colour",
                "required": false
            },
            {
                "feature_id": 105,
                "name": "Size",
                "note": "S, M, L, XL etc.",
                "required": false
            }
        ]
    }
}
```

---

## Categories Features: Browse

**Method:** `GET`

**URL:** `{{host}}/categories/{{category_id}}/features?site_id=2000&limit=118&offset=70`

**Authentication:** Required

**Example Response:**
```json
{
    "results": [
        {
            "name": "Size",
            "feature_id": 4149925,
            "group_id": 0,
            "required": false,
            "options": [
                {
                    "option_id": 18137154,
                    "name": "Small"
                },
                {
                    "option_id": 18137156,
                    "name": "Medium"
                },
                {
                    "option_id": 18137157,
                    "name": "Large"
                }
            ]
        },
        {
            "name": "Keywords",
            "feature_id": 4149926,
            "group_id": 0,
            "required": false,
            "options": [
                {
                    "option_id": 18137158,
                    "name": "Memory Foam"
                },
                {
                    "option_id": 18137160,
                    "name": "Waterproof"
                },
                {
                    "option_id": 18137161,
                    "name": "Orthopaedic"
                },
                {
                    "option_id": 18137162,
                    "name": "Donut"
                },
                {
                    "option_id": 18137163,
                    "name": "Washable"
                },
                {
                    "option_id": 18137165,
                    "name": "Raised"
                }
            ]
        }
    ],
    "metadata": {
        "limit": 20,
        "offset": 0,
        "total_rows": 2
    }
}
```

---

## Categories Technical Details: Browse Groups

**Method:** `GET`

**URL:** `{{host}}/categories/{{category_id}}/technical-details?site_id=2000&limit=8&offset=23`

**Authentication:** Required

**Example Response:**
```json
{
    "results": [
        {
            "group_id": "2",
            "group_name": "Office Chair Dimensions",
            "options": [
                {
                    "detail_id": "4",
                    "name": "Seat Width",
                    "units": [
                        "m",
                        "cm",
                        "mm",
                        "in"
                    ]
                },
                {
                    "detail_id": "5",
                    "name": "Seat Depth",
                    "units": [
                        "m",
                        "cm",
                        "mm",
                        "in"
                    ]
                },
                {
                    "detail_id": "6",
                    "name": "Back Width",
                    "units": [
                        "m",
                        "cm",
                        "mm",
                        "in"
                    ]
                },
                {
                    "detail_id": "7",
                    "name": "Back Height",
                    "units": [
                        "m",
                        "cm",
                        "mm",
                        "in"
                    ]
                },
                {
                    "detail_id": "8",
                    "name": "Seat Height",
                    "units": [
                        "m",
                        "cm",
                        "mm",
                        "in"
                    ]
                }
            ]
        }
    ],
    "metadata": {
        "limit": 10,
        "offset": 0,
        "total_results": 1
    }
}
```

---

## Categories Technical Details: View Group

**Method:** `GET`

**URL:** `{{host}}/categories/{{category_id}}/technical-details/{{technical_detail_group_id}}?site_id=2000&product_detail_group_id=234`

**Authentication:** Required

**Example Response:**
```json
{
  "results": {
    "group_id": "2",
    "group_name": "Office Chair Dimensions",
    "options": [
      {
        "detail_id": "4",
        "name": "Seat Width",
        "units": [
          "m",
          "cm",
          "mm",
          "in"
        ]
      },
      {
        "detail_id": "5",
        "name": "Seat Depth",
        "units": [
          "m",
          "cm",
          "mm",
          "in"
        ]
      },
      {
        "detail_id": "6",
        "name": "Back Width",
        "units": [
          "m",
          "cm",
          "mm",
          "in"
        ]
      },
      {
        "detail_id": "7",
        "name": "Back Height",
        "units": [
          "m",
          "cm",
          "mm",
          "in"
        ]
      },
      {
        "detail_id": "8",
        "name": "Seat Height",
        "units": [
          "m",
          "cm",
          "mm",
          "in"
        ]
      }
    ]
  }
}
```

---

