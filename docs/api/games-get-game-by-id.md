---
layout: page
---

# Get game by ID

Returns a specific [`game`](games.md) object by its unique ID.

## URL
```
GET {base_url}/games/{id}
```

## Request parameters

| Parameter | Type | Required | Description |
| ---------- | ------ | ---------- | ------------ |
| `id` | number | Yes | The unique identifier of the game to retrieve |

## Request headers

None

## Request body

None

## Return body

Returns a single game object.

Example (getting game with ID 1):
```json
{
  "title": "Battlefield 6",
  "release_date": "10-Oct-2025",
  "category": "first person shooter",
  "price": "$69.99",
  "publisher": "Electronic Arts",
  "id": 1
}
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Request successful |
| 404 | Error | Game ID not found |
| ECONNREFUSED | N/A | Service is offline. Start the service and try again. |