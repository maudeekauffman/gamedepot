---
layout: page
title: Delete a Game
parent: Tutorials
nav_order: 3
---

# Tutorial: Delete a game

In this tutorial, you will learn how to delete a game from the GameDepot database using Postman.

**Time to complete:** 5 minutes

## Prerequisites

* GameDepot API server running locally (see [Quickstart](../index.md#quickstart)).
* Postman desktop app installed.
* At least one game in the database that you want to delete.

## Step 1: Find the game ID

First, you need to know the ID of the game you want to delete.

1. In Postman, create a new **GET** request to:
```
http://localhost:3000/games
```
2. Click **Send**.
3. Find the game you want to delete and note its `id` value.

## Step 2: Create the delete request

1. Click **+** to open a new request tab.
2. Change the request method from **GET** to **DELETE** using the drop-down list.
3. Enter this URL, replacing `1` with your game's ID:
```
http://localhost:3000/games/1
```

## Step 3: Send the request

1. Click **Send**.
2. You should see a `200 OK` status.
3. The response body will show an empty object:
```json
{}
```

## Step 4: Verify the deletion

1. Create a new **GET** request to:
```
http://localhost:3000/games
```
2. Click **Send**.
3. Confirm the game no longer appears in the list.

## Next steps

* [Add a new game](add-a-game.md) - Learn how to add a game to the database.
* [API Reference: Delete a Game](../api/games-delete-game.md) - See the full endpoint documentation.