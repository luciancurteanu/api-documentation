# Product Listings

## Product Listings: Create Batch

**Method:** `POST`

**URL:** `{{host}}/listings`

**Authentication:** Required

**Example Response:**
```json
{
    "success": true,
    "results": [
        {
            "success": true,
            "created": true,
            "product_listing_id": "144083098",
            "opc": "P66TD65",
            "sku": "OAK-SMALL",
            "condition": "new"
        },
        {
            "success": true,
            "created": true,
            "product_listing_id": "144083099",
            "opc": "PDT7TXK",
            "sku": "toaster00213",
            "condition": "refurbished"
        }
    ]
}
```

---

## Product Listings: Create

**Method:** `POST`

**URL:** `{{host}}/products/{{opc}}/listings`

**Authentication:** Required

---

## Product Listings: Browse

**Method:** `GET`

**URL:** `{{host}}/listings?limit=100&offset=0&site_id=2000`

**Authentication:** Required

**Example Response:**
```json
{
    "results": [
        {
            "name": "Mini Electric Walnut Cake Maker Automatic Nut Waffle Bread Machine Sandwich Iron Toaster Baking",
            "sku": "OAK-SMALL11111",
            "group_sku": "OAK-TABLE-1",
            "price": "199.99",
            "stock": 0,
            "product_listing_id": 144083223,
            "product_listing_condition_id": 1,
            "condition": "New",
            "handling_time": 1,
            "boost_marketing_commission": "5.0",
            "product_encoded_id": "PDT729K",
            "delivery_weight": "22.0000",
            "delivery_template_id": 1061,
            "opc": "PDT729K",
            "product_url": "https://www.onbuy.com/gb/p/mini-electric-walnut-cake-maker-automatic-nut-waffle-bread-machine-sandwich-iron-toaster-baking~p104243399?preview=1",
            "image_url": "https://onbuy.com/files/default/product/thumb/default.jpg",
            "product_codes": [
                "9134478266154"
            ],
            "condition_note_1": null,
            "condition_note_2": null,
            "condition_note_3": null,
            "condition_note_4": null,
            "condition_note_5": null,
            "warranty": 12,
            "return_time": 30,
            "free_returns": 0,
            "sale_price": "149.99",
            "sale_start_date": "2024-01-01 00:00:00",
            "sale_end_date": "2024-12-31 00:00:00",
            "created_at": "2024-05-08 08:18:04",
            "updated_at": "2024-05-08 08:18:04"
        },
        {
            "name": "vidaXL Solid Teak Wood Coffee Table Living Room Furniture Wooden Side Table",
            "sku": "OAK-SMALL",
            "group_sku": "OAK-TABLE-1",
            "price": "199.99",
            "stock": 0,
            "product_listing_id": 144083098,
            "product_listing_condition_id": 1,
            "condition": "New",
            "handling_time": 1,
            "boost_marketing_commission": "5.0",
            "product_encoded_id": "P66TD65",
            "delivery_weight": "22.0000",
            "delivery_template_id": 1061,
            "opc": "P66TD65",
            "product_url": "https://www.onbuy.com/gb/p/vidaxl-solid-teak-wood-coffee-table-living-room-furniture-wooden-side-table~p25033685",
            "image_url": "https://onbuy.com/files/default/product/thumb/default.jpg",
            "product_codes": [
                "8719883910888"
            ],
            "condition_note_1": null,
            "condition_note_2": null,
            "condition_note_3": null,
            "condition_note_4": null,
            "condition_note_5": null,
            "warranty": 12,
            "return_time": 30,
            "free_returns": 0,
            "sale_price": "149.99",
            "sale_start_date": "2024-01-01 00:00:00",
            "sale_end_date": "2024-12-31 00:00:00",
            "created_at": "2024-05-08 08:10:14",
            "updated_at": "2024-05-08 08:10:14"
        },
        {
            "name": "Toaster, 2 Slice, Stainless Steel Bread Toaster with Touchscreen LCD Display, 6 Bread Options with 3 Basic Functions and More Time Functions",
            "sku": "toaster00213",
            "group_sku": null,
            "price": "49.99",
            "stock": 0,
            "product_listing_id": 144083099,
            "product_listing_condition_id": 14,
            "condition": "Refurbished",
            "handling_time": 0,
            "boost_marketing_commission": "5.0",
            "product_encoded_id": "PDT7TXK",
            "delivery_weight": "0.0000",
            "delivery_template_id": 1061,
            "opc": "PDT7TXK",
            "product_url": "https://www.onbuy.com/gb/p/toaster-2-slice-stainless-steel-bread-toaster-with-touchscreen-lcd-display-6-bread-options-with-3-basic-functions-and-more-time-functions~p104257387?condition=refurbished",
            "image_url": "https://onbuy.com/files/default/product/thumb/default.jpg",
            "product_codes": [
                ""
            ],
            "condition_note_1": "condition note 1",
            "condition_note_2": "condition note 2",
            "condition_note_3": "condition note 3",
            "condition_note_4": null,
            "condition_note_5": null,
            "warranty": 0,
            "return_time": 0,
            "free_returns": 0,
            "sale_price": null,
            "sale_start_date": null,
            "sale_end_date": null,
            "created_at": "2024-05-08 08:10:14",
            "updated_at": "2024-05-08 08:10:14"
        },
        {
            "name": "VOLVO V60 MK1 CD Radio Player Head Unit P31328970AA 31310833AA 31328970AA 2011",
            "sku": "CF-HK-MR-TV",
            "group_sku": "",
            "price": "0.00",
            "stock": 0,
            "product_listing_id": 143321157,
            "product_listing_condition_id": 14,
            "condition": "Refurbished",
            "handling_time": 0,
            "boost_marketing_commission": "5.0",
            "product_encoded_id": "P9RKRVH",
            "delivery_weight": "0.0000",
            "delivery_template_id": 1061,
            "opc": "P9RKRVH",
            "product_url": "https://www.onbuy.com/gb/p/volvo-v60-mk1-cd-radio-player-head-unit-p31328970aa-31310833aa-31328970aa-2011~p67873661?condition=refurbished",
            "image_url": "https://onbuy.com/files/default/product/thumb/default.jpg",
            "product_codes": [
                ""
            ],
            "condition_note_1": "",
            "condition_note_2": "",
            "condition_note_3": "",
            "condition_note_4": "",
            "condition_note_5": "",
            "warranty": 0,
            "return_time": 0,
            "free_returns": 0,
            "sale_price": null,
            "sale_start_date": null,
            "sale_end_date": null,
            "created_at": "2024-04-19 10:47:37",
            "updated_at": "2024-04-19 10:50:02"
        },
        {
            "name": "Just Cavalli Beachwear Y35 151 RMC Black Men L",
            "sku": "Y35151RMC_01BLACK__L",
            "group_sku": null,
            "price": "87.66",
            "stock": 145,
            "product_listing_id": 142504069,
            "product_listing_condition_id": 1,
            "condition": "New",
            "handling_time": 4,
            "boost_marketing_commission": "5.0",
            "product_encoded_id": "PDNMC9N",
            "delivery_weight": "0.0000",
            "delivery_template_id": 1061,
            "opc": "PDNMC9N",
            "product_url": "https://www.onbuy.com/gb/p/just-cavalli-beachwear-y35-151-rmc-black-men-l~p102156589?preview=1",
            "image_url": "https://onbuy.com/files/default/product/thumb/default.jpg",
            "product_codes": [
                "5003790661692"
            ],
            "condition_note_1": null,
            "condition_note_2": null,
            "condition_note_3": null,
            "condition_note_4": null,
            "condition_note_5": null,
            "warranty": 0,
            "return_time": 0,
            "free_returns": 0,
            "sale_price": null,
            "sale_start_date": null,
            "sale_end_date": null,
            "created_at": "2024-04-06 03:34:12",
            "updated_at": "2024-04-06 03:34:12"
        }
    ],
    "metadata": {
        "limit": 100,
        "offset": 0,
        "total_rows": 5
    }
}
```

---

## Product Listings: Update by SKU

**Method:** `PUT`

**URL:** `{{host}}/listings/by-sku`

**Authentication:** Required

**Example Response:**
```json
{
    "success": true,
    "results": [
        {
            "sku": "SKU1",
            "price": "399.99",
            "stock": "0",
            "handling_time_override": "1",
            "boost_marketing_commission": 0,
            "delivery_weight": 22,
            "return_time": 30,
            "free_returns": false,
            "warranty": 12,
            "sale_price": 149.99,
            "sale_start_date": "2024-01-01 00:00:00",
            "sale_end_date": "2024-12-31 00:00:00",
            "group_sku": "OAK-TABLE-1",
            "delivery_template_id": 1061,
            "product_listing_id": "144087627"
        },
        {
            "sku": "SKU2",
            "price": "17.66",
            "stock": 1,
            "product_listing_id": "144087626"
        }
    ]
}
```

---

## Product Listings: Delete by SKU

**Method:** `DELETE`

**URL:** `{{host}}/listings/by-sku`

**Authentication:** Required

**Example Response:**
```json
{
    "success": true,
    "results": {
        "TEST-SKU-SKIMMER": {
            "error": "SKU not found"
        },
        "PPL-SKU18293": {
            "status": "ok"
        }
    }
}
```

---

## Product Listings: Check Winning

**Method:** `GET`

**URL:** `{{host}}/listings/check-winning?site_id=2000&skus=[]`

**Authentication:** Required

**Example Response:**
```json
{
    "success": true,
    "results": [
        {
            "sku": "New listing 1",
            "price": "1.00",
            "item_price": null,
            "delivery_price": null,
            "lead_price": null,
            "lead_item_price": null,
            "lead_delivery_price": null,
            "winning": false
        },
        {
            "sku": "new listing 2",
            "price": "1.00",
            "item_price": null,
            "delivery_price": null,
            "lead_price": null,
            "lead_item_price": null,
            "lead_delivery_price": null,
            "winning": false
        }
    ]
}
```

---

