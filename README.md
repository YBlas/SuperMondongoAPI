# SuperHeroes API

This is a simple API built with Deno and Express for managing superheroes data in a MongoDB database.

## Getting Started

To run this API locally, follow these steps:

### Prerequisites

- [Deno](https://deno.land/#installation)
- MongoDB database

### Installation

1. Clone this repository:

```bash
git clone <repository-url>
Install dependencies:
bash
Copy code
deno cache --reload --lock=lock.json --lock-write mod.ts
Set up environment variables by creating a .env file in the root directory and adding the following:
bash
Copy code
PASS=your_mongodb_password
USER=your_mongodb_username
Replace your_mongodb_password and your_mongodb_username with your MongoDB credentials.

Running the API
bash
Copy code
deno run --allow-net --allow-read --allow-env mod.ts
The API should now be running on port 3000.

Endpoints
GET /
Retrieve all superheroes.

Example
http
Copy code
GET http://localhost:3000/
GET /:name
Retrieve superheroes by name (case-insensitive).

Example
http
Copy code
GET http://localhost:3000/spider
POST /
Create a new superhero.

Request Body
json
Copy code
{
  "name": "Spider-Man",
  "image": "https://example.com/spiderman.jpg",
  "sound": "https://example.com/spiderman_sound.mp3"
}
Example
http
Copy code
POST http://localhost:3000/
Content-Type: application/json

{
  "name": "Spider-Man",
  "image": "https://example.com/spiderman.jpg",
  "sound": "https://example.com/spiderman_sound.mp3"
}
Error Handling
400 Bad Request: If the request body is missing any required fields or if the superhero name is repeated.
404 Not Found: If the requested resource is not found.
Dependencies
Express - Web framework for Node.js
MongoDB - NoSQL database
dotenv - Loads environment variables from a .env file
mongo - MongoDB driver for Deno
std - Standard library for Deno
License
This project is licensed under the MIT License - see the LICENSE file for details.
