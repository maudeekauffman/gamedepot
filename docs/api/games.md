---
layout: page
title: Games Resource
parent: API Reference
nav_order: 1
---

# games resource

Base endpoint:
```
{base_url}/games
```

Contains information about video games in the GameDepot database.

## Resource properties

Sample `games` resource:
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

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `title` | string | The name of the game |
| `release_date` | string | When the game was released |
| `category` | string | The game's genre (e.g., "first person shooter," "city builder") |
| `price` | string | Current retail price |
| `publisher` | string | Company that published the game |
| `id` | number | Unique identifier for the game |

## Operations

The `games` resource supports these operations:

### READ (GET)

* [Get all games](games-get-all-games.md)
* [Get game by ID](games-get-game-by-id.md)