---
layout: page
title: Create a Game
parent: API Reference
nav_order: 4
---

# Create a game

Adds a new game to the GameDepot database.

## URL
```
POST {base_url}/games
```

## Request parameters

None

## Request headers

| Header | Value | Required |
| ------ | ----- | -------- |
| Content-Type | application/json | Yes |

## Request body

A JSON object containing the game properties.

| Property | Type | Required | Description |
| -------- | ---- | -------- | ----------- |
| title | string | Yes | The name of the game |
| release_date | string | Yes | Release date in DD-MMM-YYYY format |
| category | string | Yes | Game genre (e.g., "first person shooter," "real-time strategy") |
| price | string | Yes | Price including currency symbol (e.g., "$59.99") |
| publisher | string | Yes | Name of the game publisher |

Example:
```json
{
  "title": "Starfield",
  "release_date": "06-Sep-2023",
  "category": "role-playing game",
  "price": "$69.99",
  "publisher": "Bethesda Softworks"
}
```

## Return body

Returns the newly created game object with an assigned `id`.

Example:
```json
{
  "title": "Starfield",
  "release_date": "06-Sep-2023",
  "category": "role-playing game",
  "price": "$69.99",
  "publisher": "Bethesda Softworks",
  "id": 5
}
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 201 | Created | Game successfully added |
| 400 | Bad Request | Invalid or missing request body |
| ECONNREFUSED | N/A | Service is offline. Start the service and try again. |