# Sites

Site endpoints provide information about OnBuy's regional variations and localization settings.

## Overview

OnBuy operates in multiple regions with different site IDs. Each site has its own localization, currency, and operational settings.

## Sites: Browse

Get a list of all OnBuy regional sites.

**Method:** `GET`

**URL:** `{{host}}/sites`

**Authentication:** Required

**Parameters:**

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| filter[name] | string | No | Filter sites by name |
| limit | integer | No | Number of results to return (max 100) |
| offset | integer | No | Starting record for pagination |

**Example Request:**
```bash
curl -X GET "https://api.onbuy.com/v2/sites?offset=0&limit=100" \
  -H "Authorization: YOUR_ACCESS_TOKEN"
```

**Example Response:**
```json
{
    "results": [
        {
            "site_id": 2000,
            "name": "OnBuy UK",
            "country_code": "gb",
            "default_localisation": "en-GB"
        }
    ],
    "metadata": {
        "limit": 100,
        "offset": 0,
        "total_rows": 1
    }
}
```

---

## Sites: View

Get details for a specific OnBuy regional site.

**Method:** `GET`

**URL:** `{{host}}/sites/{{site_id}}`

**Authentication:** Required

**Parameters:**

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| site_id | integer | Yes | The ID of the OnBuy regional site |

**Example Request:**
```bash
curl -X GET "https://api.onbuy.com/v2/sites/2000" \
  -H "Authorization: YOUR_ACCESS_TOKEN"
```

**Example Response:**
```json
{
    "data": {
        "site_id": "2000",
        "name": "OnBuy UK"
    }
}
```

## Available Sites

| Site ID | Name | Country Code | Localization |
|---------|------|--------------|--------------|
| 2000 | OnBuy UK | gb | en-GB |

---
