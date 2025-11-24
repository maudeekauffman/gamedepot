---
layout: page
title: Get All Games
parent: API Reference
nav_order: 2
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
    "image": "https://upload.wikimedia.org/wikipedia/commons/thumb/8/8e/Battlefield_1_logo.png/220px-Battlefield_1_logo.png",
    "id": 1
  },
  {
    "title": "Mechabellum",
    "release_date": "26-Sep-2024",
    "category": "real-time strategy",
    "price": "$14.79",
    "publisher": "Dreamhaven",
    "image": "https://shared.akamai.steamstatic.com/store_item_assets/steam/apps/669330/header.jpg",
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