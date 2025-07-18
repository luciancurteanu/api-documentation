# Queues

Queue endpoints allow you to monitor the status of asynchronous operations, primarily product creation.

## Overview

When you create products via the API, they are added to a processing queue. Use these endpoints to check the status of queued operations.

**Queue Statuses:**
- **pending**: Operation is waiting to be processed
- **success**: Operation completed successfully
- **failed**: Operation failed with error details

## Queues: Browse

Get the status of multiple queue items.

**Method:** `GET`

**URL:** `{{host}}/queues`

**Authentication:** Required

**Parameters:**

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| site_id | integer | Yes | Target site ID |
| filter[queue_ids] | string | No | Comma-separated list of queue IDs |
| filter[status] | string | No | Filter by status (`pending`, `success`, `failed`) |
| limit | integer | No | Results per page (max 100) |
| offset | integer | No | Starting record |

**Example Request:**
```bash
curl -X GET "https://api.onbuy.com/v2/queues?site_id=2000&filter[status]=pending" \
  -H "Authorization: YOUR_ACCESS_TOKEN"
```

**Example Response:**
```json
{
    "results": [
        {
            "queue_id": "5a004bbc46145c21dc006866",
            "status": "pending"
        },
        {
            "queue_id": "5a057eab2c5e138f5c000d43",
            "status": "success",
            "opc": "P7ZV78"
        },
        {
            "queue_id": "5a057eac2c5e138f5c000d46",
            "status": "failed",
            "error_message": "Product code \"5011479102725\" already exists",
            "existing_opc": "P7ZX58"
        }
    ],
    "metadata": {
        "limit": 10,
        "offset": 0,
        "total_rows": 45
    }
}
```

---

## Queues: View

Get the status of a specific queue item.

**Method:** `GET`

**URL:** `{{host}}/queues/{{queue_id}}`

**Authentication:** Required

**Parameters:**

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| queue_id | string | Yes | The queue ID to check |
| site_id | integer | Yes | Target site ID |

**Example Request:**
```bash
curl -X GET "https://api.onbuy.com/v2/queues/59f751b246145c0ef8001147?site_id=2000" \
  -H "Authorization: YOUR_ACCESS_TOKEN"
```

**Example Response:**
```json
{
    "results": {
        "queue_id": "59f751b246145c0ef8001147",
        "status": "failed",
        "error_message": "Product code \"9783598215063\" already exists"
    }
}
```

## Usage Tips

- **Polling**: Check queue status periodically, but avoid excessive requests
- **Batch Processing**: Use browse endpoint to check multiple queues at once
- **Error Handling**: Failed queues include error messages for troubleshooting
- **Success Response**: Successful product creation returns the assigned OPC

---

