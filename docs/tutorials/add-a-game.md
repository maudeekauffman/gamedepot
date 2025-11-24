---
layout: page
title: "Tutorial: Add a New Game"
nav_order: 3
---

# Tutorial: Add a new game

In this tutorial, you'll learn how to add a new game to the GameDepot database using Postman.

**Time to complete:** 10 minutes

## Prerequisites

* GameDepot API server running locally (see [Quickstart](../index.md#quickstart))
* Postman desktop app installed

## Step 1: Open Postman

Launch the Postman desktop app on your computer.

## Step 2: Create a new request

1. Click the **+** button to open a new request tab
2. Change the request method from **GET** to **POST** using the dropdown
3. Enter this URL:
```
http://localhost:3000/games
```

## Step 3: Set the request headers

1. Click the **Headers** tab
2. Add a new header:
   * Key: `Content-Type`
   * Value: `application/json`

## Step 4: Add the request body

1. Click the **Body** tab
2. Select **raw**
3. Make sure **JSON** is selected in the dropdown
4. Paste this JSON:
```json
{
  "title": "The Legend of Zelda: Tears of the Kingdom",
  "release_date": "12-May-2023",
  "category": "action-adventure",
  "price": "$69.99",
  "publisher": "Nintendo"
}
```

## Step 5: Send the request

1. Click **Send**
2. You should see a `201 Created` status
3. The response body will show your new game with an assigned `id`:
```json
{
  "title": "The Legend of Zelda: Tears of the Kingdom",
  "release_date": "12-May-2023",
  "category": "action-adventure",
  "price": "$69.99",
  "publisher": "Nintendo",
  "id": 5
}
```

## Step 6: Verify the game was added

1. Create a new **GET** request to:
```
http://localhost:3000/games
```
2. Click **Send**
3. You should see your new game in the list of all games

## Next steps

* [Update a game](../api/games-update-game.md) - Learn how to modify game information
* [Delete a game](../api/games-delete-game.md) - Learn how to remove a game from the database