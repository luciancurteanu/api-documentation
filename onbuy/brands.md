# Brands

Brand management endpoints allow you to browse and view brand information for products listed on OnBuy.

## Overview

Brands are used to categorize products by manufacturer or brand name. You can search for existing brands when creating products to ensure consistency.

## Brands: Browse

Search and browse available brands on OnBuy.

**Method:** `GET`

**URL:** `{{host}}/brands`

**Authentication:** Required

**Parameters:**

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| filter[name] | string | Yes | The name of the brand to search for |
| sort[name] | string | No | Sort by brand name (`asc` or `desc`) |
| limit | integer | No | Number of results to return (max 100) |
| offset | integer | No | Starting record for pagination |

**Example Request:**
```bash
curl -X GET "https://api.onbuy.com/v2/brands?filter[name]=life&sort[name]=desc&limit=5&offset=0" \
  -H "Authorization: YOUR_ACCESS_TOKEN"
```

**Example Response:**
```json
{
    "results": [
        {
            "brand_id": "3675",
            "name": "Vitalife",
            "brand_type_id": "1",
            "type": "Standard"
        },
        {
            "brand_id": "3694",
            "name": "Tree Of Life",
            "brand_type_id": "1",
            "type": "Standard"
        },
        {
            "brand_id": "891",
            "name": "The Secret Life of Pets",
            "brand_type_id": "1",
            "type": "Standard"
        },
        {
            "brand_id": "3766",
            "name": "Superlife",
            "brand_type_id": "1",
            "type": "Standard"
        },
        {
            "brand_id": "3085",
            "name": "Petlife",
            "brand_type_id": "1",
            "type": "Standard"
        }
    ],
    "metadata": {
        "limit": 5,
        "offset": 0,
        "total_rows": "18",
        "filters": {
            "name": "life"
        },
        "sort": {
            "name": "desc"
        }
    }
}
```

---

## Brands: View

Get details for a specific brand by ID.

**Method:** `GET`

**URL:** `{{host}}/brands/{{brand_id}}`

**Authentication:** Required

**Parameters:**

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| brand_id | integer | Yes | The unique ID of the brand |

**Example Request:**
```bash
curl -X GET "https://api.onbuy.com/v2/brands/3058" \
  -H "Authorization: YOUR_ACCESS_TOKEN"
```

**Example Response:**
```json
{
    "results": {
        "brand_id": "3058",
        "name": "Perfect Pools",
        "brand_type_id": "2",
        "type": "Store"
    }
}
```

## Brand Types

| Type ID | Type | Description |
|---------|------|-------------|
| 1 | Standard | Regular manufacturer brands |
| 2 | Store | OnBuy seller store brands |

---

