# Sellers Entities

## Sellers Entities: Browse

**Method:** `GET`

**URL:** `{{host}}/sellers/entities?limit=44&offset=11`

**Authentication:** Required

**Example Response:**
```json
{
    "data": [
        {
            "entity_id": "001",
            "trading_name": "Example Trading Name"
        }
    ],
    "metadata": {
        "limit": 5,
        "offset": 0,
        "total_results": 1
    }
}


```

---

## Sellers Entities: View

**Method:** `GET`

**URL:** `{{host}}/sellers/entities/{{entity_id}}?limit=0&offset=229`

**Authentication:** Required

**Example Response:**
```json
{
    "data": {
        "entity_id": "001",
        "trading_name": "Example Trading Name"
    }
}
```

---

