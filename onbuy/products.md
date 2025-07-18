# Products

Product endpoints allow you to create, search, and manage products on the OnBuy marketplace.

## Overview

Products on OnBuy have a two-stage creation process:
1. **Product Creation**: Submit product data for validation
2. **Queue Processing**: Monitor the creation queue for completion status

## Key Concepts

- **OPC (OnBuy Product Code)**: Unique identifier assigned to each product
- **GTIN/EAN**: Global Trade Item Number for product identification
- **Product Approval**: Products require approval before going live
- **Image Requirements**: Product images must be accessible for download

## Products: Search

Search for existing products on OnBuy.

**Method:** `GET`

**URL:** `{{host}}/products`

**Authentication:** Required

**Parameters:**

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| filter[ean] | string | No | EAN/GTIN to search for |
| filter[opc] | string | No | OnBuy Product Code |
| filter[title] | string | No | Product title to search |
| site_id | integer | Yes | Target site ID |
| limit | integer | No | Results per page (max 100) |
| offset | integer | No | Starting record |

---

## Products: Create

Create a new product on OnBuy.

**Method:** `POST`

**URL:** `{{host}}/products`

**Authentication:** Required

**Content-Type:** `application/json`

**Request Body Example:**
```json
{
    "site_id": 2000,
    "gtin": "1234567890123",
    "title": "Example Product",
    "description": "Detailed product description",
    "category_id": 1234,
    "brand_id": 567,
    "images": [
        "https://example.com/image1.jpg",
        "https://example.com/image2.jpg"
    ],
    "product_data": {
        "weight": "1.5",
        "dimensions": {
            "length": "10",
            "width": "5",
            "height": "3"
        }
    }
}
```

**Response:**
```json
{
    "queue_id": "abc123-def456-ghi789"
}
```

## Image Download Requirements

OnBuy needs to download images from your media service. Ensure these IP addresses are allowlisted:

- **34.142.64.77**
- **34.142.18.212**
- **35.246.83.100**
- **34.105.246.78**

## Test Products

- Test products can be created using test API credentials
- Test and live product databases are shared for GTIN validation
- Use test credentials to verify product creation process

---
