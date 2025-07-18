# Carriers

Carrier endpoints provide information about supported shipping carriers for order dispatch.

## Overview

Carriers are used when dispatching orders to specify which shipping service was used. This helps with tracking and delivery management.

## Carriers: Browse

Get a list of all supported carriers, with optional filtering by name.

**Method:** `GET`

**URL:** `{{host}}/carriers`

**Authentication:** Required

**Parameters:**

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| site_id | integer | Yes | Target site ID (default: 2000 for UK) |
| filter[name] | string | No | Partial or full carrier name to search for |

**Example Request:**
```bash
curl -X GET "https://api.onbuy.com/v2/carriers?site_id=2000&filter[name]=royal" \
  -H "Authorization: YOUR_ACCESS_TOKEN"
```

**Example Response:**
```json
[
    {
        "onbuy_carrier_code": "OCC-MHUBGIUW4UH9ES5I6D",
        "carrier_name": "Royal Mail"
    },
    {
        "onbuy_carrier_code": "OCC-JXX0730DR15E0U4Y06",
        "carrier_name": "RoyalShipments"
    }
]
```

## Usage Notes

- Use the `onbuy_carrier_code` when dispatching orders
- Carrier codes are unique identifiers for tracking purposes
- Different sites may have different available carriers

---
