---
layout: page
title: Update a Game
parent: API Reference
nav_order: 5
---

# Update a game

Updates an existing game in the GameDepot database.

## URL
```
PUT {base_url}/games/{id}
```

## Request parameters

| Parameter | Type | Required | Description |
| --------- | ---- | -------- | ----------- |
| id | integer | Yes | The unique ID of the game to update |

## Request headers

| Header | Value | Required |
| ------ | ----- | -------- |
| Content-Type | application/json | Yes |

## Request body

A JSON object containing all game properties (PUT replaces the entire resource).

| Property | Type | Required | Description |
| -------- | ---- | -------- | ----------- |
| title | string | Yes | The name of the game |
| release_date | string | Yes | Release date in DD-MMM-YYYY format |
| category | string | Yes | Game genre (e.g., "first person shooter," "real-time strategy") |
| price | string | Yes | Price including currency symbol (e.g., "$59.99") |
| publisher | string | Yes | Name of the game publisher |
| image | string | No | URL to the game's cover image |

Example:
```json
{
  "title": "Battlefield 6",
  "release_date": "10-Oct-2025",
  "category": "first person shooter",
  "price": "$49.99",
  "publisher": "Electronic Arts",
  "image": "https://upload.wikimedia.org/wikipedia/commons/thumb/8/8e/Battlefield_1_logo.png/220px-Battlefield_1_logo.png"
}
```

## Return body

Returns the updated game object.

Example:
```json
{
  "title": "Battlefield 6",
  "release_date": "10-Oct-2025",
  "category": "first person shooter",
  "price": "$49.99",
  "publisher": "Electronic Arts",
  "image": "https://upload.wikimedia.org/wikipedia/commons/thumb/8/8e/Battlefield_1_logo.png/220px-Battlefield_1_logo.png",
  "id": 1
}
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Game successfully updated |
| 400 | Bad Request | Invalid or missing request body |
| 404 | Not Found | Game with specified ID not found |
| ECONNREFUSED | N/A | Service is offline. Start the service and try again. |