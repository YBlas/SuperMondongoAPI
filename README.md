Endpoints Documentation

1. GET /
   Description: Retrieves all superheroes stored in the database.
   Method: GET
   URL: /
   Response: An array of superhero objects in JSON format.
2. GET /:name
   Description: Retrieves superheroes whose name matches the provided query string.
   Method: GET
   URL: /:name
   Parameters:
   name: The name of the superhero to search for.
   Response: An array of superhero objects in JSON format whose name matches the provided query string.
3. POST /
   Description: Adds a new superhero to the database.
   Method: POST
   URL: /
   Request Body:
   name: Name of the superhero (required)
   image: URL of the superhero's image (required)
   sound: URL of the superhero's sound (required)
   creator: Name of the creator of the superhero (required)
   Response:
   201 Created if the superhero is successfully added, along with the \_id of the newly added superhero.
   400 Bad Request if any required field is missing in the request body.
4. DELETE /:name
   Description: Deletes a superhero from the database by name and creator.
   Method: DELETE
   URL: /:name
   Parameters:
   name: The name of the superhero to delete.
   Request Body:
   creator: Name of the creator of the superhero (required)
   Response:
   204 No Content if the superhero is successfully deleted.
   400 Bad Request if the creator field is missing in the request body.
   404 Not Found if the superhero with the specified name and creator is not found in the database.
