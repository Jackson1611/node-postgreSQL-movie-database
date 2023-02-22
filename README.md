# Movie API

This is a simple RESTful API for managing movies. It allows you to create, read, update, and delete movies.

## Getting Started

To get started, clone this repository and run `npm install` to install the dependencies.

Next, create a `.env` file in the root directory of the project and add the following variables:

DB_HOST=localhost
DB_PORT=5432
DB_NAME=movie_db
DB_USER=myusername
DB_PASSWORD=mypassword

Make sure to replace the values with your own database connection information.

Then, run the following command to start the server:

npm start

The server should now be running on `http://localhost:3000`.

## Endpoints

The API has the following endpoints:

- `GET /api/movies` - Get all movies
- `GET /api/movies/:id` - Get a movie by ID
- `POST /api/movies` - Add a new movie
- `PUT /api/movies/:id` - Update a movie
- `DELETE /api/movies/:id` - Delete a movie

### Example Requests

Here are some example requests you can make using `curl`:

Get all movies:
curl http://localhost:3000/api/movies

Get a movie by ID:
curl http://localhost:3000/api/movies/1

Add a new movie:
curl -X POST -H "Content-Type: application/json" -d '{"title":"The Shawshank Redemption", "director":"Frank Darabont", "year":1994}' http://localhost:3000/api/movies

Update a movie:
curl -X PUT -H "Content-Type: application/json" -d '{"title":"The Shawshank Redemption", "director":"Frank Darabont", "year":1994}' http://localhost:3000/api/movies/1

Delete a movie:
curl -X DELETE http://localhost:3000/api/movies/1

## License

This project is licensed under the MIT License - see the LICENSE file for details.



