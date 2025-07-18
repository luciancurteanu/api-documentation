# Orders

Order endpoints allow you to browse, view, and manage orders from your OnBuy account.

## Overview

Orders go through various states from placement to completion:
1. **Pending**: Order placed, awaiting processing
2. **Dispatched**: Order shipped with tracking
3. **Delivered**: Order successfully delivered
4. **Cancelled**: Order cancelled
5. **Refunded**: Order refunded (partial or full)

## Orders: Browse

Get a list of orders with filtering and pagination.

**Method:** `GET`

**URL:** `{{host}}/orders`

**Authentication:** Required

**Parameters:**

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| site_id | integer | Yes | Target site ID |
| seller_id | integer | Yes | Your seller ID |
| filter[status] | string | No | Filter by order status |
| filter[created_from] | string | No | Orders created from date (YYYY-MM-DD) |
| filter[created_to] | string | No | Orders created to date (YYYY-MM-DD) |
| limit | integer | No | Results per page (max 100) |
| offset | integer | No | Starting record |

**Example Request:**
```bash
curl -X GET "https://api.onbuy.com/v2/orders?site_id=2000&seller_id=123" \
  -H "Authorization: YOUR_ACCESS_TOKEN"
```

---

## Orders: View

Get details for a specific order.

**Method:** `GET`

**URL:** `{{host}}/orders/{{order_id}}`

**Authentication:** Required

---

## Orders: Dispatch

Mark an order as dispatched with tracking information.

**Method:** `PUT`

**URL:** `{{host}}/orders/{{order_id}}/dispatch`

**Authentication:** Required

**Request Body:**
```json
{
    "tracking_id": "1234567890",
    "carrier_code": "OCC-MHUBGIUW4UH9ES5I6D",
    "items": [
        {
            "order_item_id": 123,
            "quantity": 1
        }
    ]
}
```

---

## Orders: Cancel

Cancel an order or specific items.

**Method:** `PUT`

**URL:** `{{host}}/orders/{{order_id}}/cancel`

**Authentication:** Required

---

## Orders: Refund

Process a refund for an order.

**Method:** `PUT`

**URL:** `{{host}}/orders/{{order_id}}/refund`

**Authentication:** Required

**Request Body:**
```json
{
    "refund_amount": "25.99",
    "refund_reason": "Customer requested return",
    "items": [
        {
            "order_item_id": 123,
            "quantity": 1
        }
    ]
}
```

## Order States

| Status | Description |
|--------|-------------|
| pending | Order awaiting processing |
| dispatched | Order has been shipped |
| delivered | Order successfully delivered |
| cancelled | Order was cancelled |
| refunded | Order has been refunded |

---
