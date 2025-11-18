---
layout: page
---

# Get all games

Returns an array of [`games`](games.md) objects that contains all games in the GameDepot database.

## URL
```
GET {base_url}/games
```

## Request parameters

None

## Request headers

None

## Request body

None

## Return body

Returns an array of all games in the database.

Example:
```json
[
  {
    "title": "Battlefield 6",
    "release_date": "10-Oct-2025",
    "category": "first person shooter",
    "price": "$69.99",
    "publisher": "Electronic Arts",
    "id": 1
  },
  {
    "title": "Mechabellum",
    "release_date": "26-Sep-2024",
    "category": "real-time strategy",
    "price": "$14.79",
    "publisher": "Dreamhaven",
    "id": 2
  }
]
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Request successful |
| 404 | Error | Resource not found |
| ECONNREFUSED | N/A | Service is offline. Start the service and try again. |