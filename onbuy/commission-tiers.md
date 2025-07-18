# Commission Tiers

## Commission Tiers: Browse

**Method:** `GET`

**URL:** `{{host}}/commission-tiers?site_id=2000`

**Authentication:** Required

**Example Response:**
```json
[
    {
        "type": "CommissionTier",
        "attributes": {
            "sales_fee_site_id": 2000,
            "sales_fee_lower_threshold_percentage": "13.50",
            "sales_fee_min_amount": 25,
            "sales_fee_name": "Arts, Crafts & Sewing",
            "sales_fee_upper_threshold_percentage": null,
            "sales_fee_threshold_amount": null,
            "sales_fee_is_standard": true,
            "sales_fee_group": "EE",
            "sales_fee_hide": false
        },
        "id": "98e7b910-ee73-440c-9eb8-56a2d9bfb505"
    },
    {
        "type": "CommissionTier",
        "attributes": {
            "sales_fee_site_id": 2000,
            "sales_fee_lower_threshold_percentage": "8.00",
            "sales_fee_min_amount": 25,
            "sales_fee_name": "Baby & Toddler",
            "sales_fee_upper_threshold_percentage": "13.50",
            "sales_fee_threshold_amount": 1000,
            "sales_fee_is_standard": true,
            "sales_fee_group": "EE",
            "sales_fee_hide": false
        },
        "id": "98e7b910-f600-4329-8501-f9b45cb913ac"
    },
    {
        "type": "CommissionTier",
        "attributes": {
            "sales_fee_site_id": 2000,
            "sales_fee_lower_threshold_percentage": "10.00",
            "sales_fee_min_amount": 25,
            "sales_fee_name": "Beer, Wine & Spirits",
            "sales_fee_upper_threshold_percentage": null,
            "sales_fee_threshold_amount": null,
            "sales_fee_is_standard": true,
            "sales_fee_group": "EE",
            "sales_fee_hide": false
        },
        "id": "98e7b911-47d0-4363-9095-5af522d564a5"
    },
    {
        "type": "CommissionTier",
        "attributes": {
            "sales_fee_site_id": 2000,
            "sales_fee_lower_threshold_percentage": "13.50",
            "sales_fee_min_amount": 25,
            "sales_fee_name": "Books",
            "sales_fee_upper_threshold_percentage": null,
            "sales_fee_threshold_amount": null,
            "sales_fee_is_standard": true,
            "sales_fee_group": "EE",
            "sales_fee_hide": false
        },
        "id": "98e7b910-ffcc-414c-9c3f-b949d7c6af00"
    },
    {
        "type": "CommissionTier",
        "attributes": {
            "sales_fee_site_id": 2000,
            "sales_fee_lower_threshold_percentage": "13.50",
            "sales_fee_min_amount": 25,
            "sales_fee_name": "Business, Office & Industrial Supplies",
            "sales_fee_upper_threshold_percentage": null,
            "sales_fee_threshold_amount": null,
            "sales_fee_is_standard": true,
            "sales_fee_group": "EE",
            "sales_fee_hide": false
        },
        "id": "98e7b911-082a-4bbf-9284-b4ab1d426c75"
    },
    {
        "type": "CommissionTier",
        "attributes": {
            "sales_fee_site_id": 2000,
            "sales_fee_lower_threshold_percentage": "13.50",
            "sales_fee_min_amount": 25,
            "sales_fee_name": "Car & Automotive Parts",
            "sales_fee_upper_threshold_percentage": "9.00",
            "sales_fee_threshold_amount": 4500,
            "sales_fee_is_standard": true,
            "sales_fee_group": "EE",
            "sales_fee_hide": false
        },
        "id": "98e7b911-12f3-4666-8b9f-60918ac8bae6"
    },
    {
        "type": "CommissionTier",
        "attributes": {
            "sales_fee_site_id": 2000,
            "sales_fee_lower_threshold_percentage": "13.50",
            "sales_fee_min_amount": 25,
            "sales_fee_name": "Clothing, Shoes & Accessories",
            "sales_fee_upper_threshold_percentage": null,
            "sales_fee_threshold_amount": null,
            "sales_fee_is_standard": true,
            "sales_fee_group": "EE",
            "sales_fee_hide": false
        },
        "id": "98e7b911-2a36-444d-95ac-484c29617bb0"
    },
    {
        "type": "CommissionTier",
        "attributes": {
            "sales_fee_site_id": 2000,
            "sales_fee_lower_threshold_percentage": "7.00",
            "sales_fee_min_amount": 25,
            "sales_fee_name": "Consumer Electronics",
            "sales_fee_upper_threshold_percentage": null,
            "sales_fee_threshold_amount": null,
            "sales_fee_is_standard": true,
            "sales_fee_group": "CEWG",
            "sales_fee_hide": false
        },
        "id": "98e7b911-0dd7-466c-89e9-1fcd7c43ac1b"
    },
    {
        "type": "CommissionTier",
        "attributes": {
            "sales_fee_site_id": 2000,
            "sales_fee_lower_threshold_percentage": "12.00",
            "sales_fee_min_amount": 25,
            "sales_fee_name": "DIY & Tools",
            "sales_fee_upper_threshold_percentage": null,
            "sales_fee_threshold_amount": null,
            "sales_fee_is_standard": true,
            "sales_fee_group": "EE",
            "sales_fee_hide": false
        },
        "id": "98e7b911-1db6-4091-b814-adc7e1876ff1"
    },
    {
        "type": "CommissionTier",
        "attributes": {
            "sales_fee_site_id": 2000,
            "sales_fee_lower_threshold_percentage": "13.50",
            "sales_fee_min_amount": 25,
            "sales_fee_name": "Electronic Accessories",
            "sales_fee_upper_threshold_percentage": "8.00",
            "sales_fee_threshold_amount": 10000,
            "sales_fee_is_standard": true,
            "sales_fee_group": "EE",
            "sales_fee_hide": false
        },
        "id": "98e7b911-23fc-4537-9914-da63b33339bb"
    }
]
```

---

## Commission Tiers: View

**Method:** `GET`

**URL:** `{{host}}/commission-tiers/98e7b910-e5f1-4ac9-aa84-f57ad8582196?site_id=2000`

**Authentication:** Required

**Example Response:**
```json
{
  "results": [
    {
      "commission_tier_id": "3",
      "site_id": "2000",
      "fee": "9.00",
      "name": "Standard Fee"
    }
  ]
}
```

---

