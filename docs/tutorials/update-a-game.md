---
layout: page
title: Update a Game
parent: Tutorials
nav_order: 2
---

# Tutorial: Update a game

In this tutorial, you will learn how to update an existing game in the GameDepot database using Postman.

**Time to complete:** 10 minutes

## Prerequisites

* GameDepot API server running locally (see [Quickstart](../index.md#quickstart)).
* Postman desktop app installed.
* At least one game in the database.

## Step 1: Find the game ID

First, you need to know the ID of the game you want to update.

1. In Postman, create a new **GET** request to:
```
http://localhost:3000/games
```
2. Click **Send**.
3. Find the game you want to update and note its `id` value.

## Step 2: Create the update request

1. Click **+** to open a new request tab.
2. Change the request method from **GET** to **PUT** using the drop-down list.
3. Enter this URL, replacing `1` with your game's ID:
```
http://localhost:3000/games/1
```

## Step 3: Set the request headers

1. Click the **Headers** tab.
2. Add a new header:
   * Key: `Content-Type`
   * Value: `application/json`

## Step 4: Add the request body

1. Click the **Body** tab.
2. Select **raw**.
3. Make sure **JSON** is selected in the drop-down list.
4. Copy and paste the complete game object with your updates. This example changes the price:
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

**Note:** PUT replaces the entire resource, so include all fields, not just the ones you want to change.

## Step 5: Send the request

1. Click **Send**.
2. You should see a `200 OK` status.
3. The response body will show the updated game:
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

## Step 6: Verify the update

1. Create a new **GET** request to:
```
http://localhost:3000/games/1
```
2. Click **Send**.
3. Confirm the game shows your updated information.

## Next steps

* [Delete a game](delete-a-game.md) - Learn how to remove a game from the database.
* [API Reference: Update a Game](../api/games-update-game.md) - See the full endpoint documentation.