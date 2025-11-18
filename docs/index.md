---
layout: page
---

# GameDepot API

This is a mock API to simulate the REST interface of an imaginary service.

GameDepot is a video game discovery service that helps users explore and find information about video games. Users can search for games by title, category, publisher, or browse by release date and price.

## Quickstart

Get started with GameDepot by retrieving your first game! 

### What you need

* A development system running Windows, MacOS, or Linux
* Git command line tools
* Node.js (current or LTS version)
* json-server version 0.17.4
* Postman desktop app

### Getting your first game

1. Start the GameDepot API server locally:
```bash
   json-server --watch to-do-db-source.json
```

2. In Postman, create a new GET request to:
```
   http://localhost:3000/games/1
```

3. Click **Send**

You should receive a JSON response with details about the first game in the database!

## API reference docs

The API reference docs refer to a `{base_url}` when they refer to the URL of a resource. The `{base_url}` value depends on the installation of the service.

When run locally for testing, the `{base_url}` is generally `http://localhost:3000`.

### Available resources

* [**games**](api/games.md) - Information about video games including title, release date, category, price, and publisher
  * [Get all games](api/games-get-all-games.md)
  * [Get game by ID](api/games-get-game-by-id.md)
* **developers** - Information about game development studios *(coming soon)*
* **publishers** - Information about game publishers *(coming soon)*

### Common operations

* Get all games: `GET {base_url}/games`
* Get a specific game: `GET {base_url}/games/{id}`
* Get all developers: `GET {base_url}/developers`
* Get all publishers: `GET {base_url}/publishers`