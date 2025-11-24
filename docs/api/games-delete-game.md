---
layout: page
title: Delete a Game
parent: API Reference
nav_order: 6
---

# Delete a game

Removes a game from the GameDepot database.

## URL
```
DELETE {base_url}/games/{id}
```

## Request parameters

| Parameter | Type | Required | Description |
| --------- | ---- | -------- | ----------- |
| id | integer | Yes | The unique ID of the game to delete |

## Request headers

None

## Request body

None

## Return body

Returns an empty object.

Example:
```json
{}
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Game successfully deleted |
| 404 | Not Found | Game with specified ID not found |
| ECONNREFUSED | N/A | Service is offline. Start the service and try again. |