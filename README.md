# Travel Echo [https://travelmemories.onrender.com/](https://travelmemories.onrender.com/)

This is a Node.js and React.js application that provides signup and authentication functionality for users. It allows users to store pictures of places they have visited in the past. Below is an overview of the project structure and key features.

## Project Structure

```sh

- app.js
- routes/
  - places-routes.js
  - users-routes.js
- models/
  - http-error.js
- uploads/
  - images/
- public/
- package.json
- README.md
```

- \`app.js\`: Main entry point of the application that sets up the server and defines middleware.
- \`routes/\`: Directory containing route handlers for different API endpoints.
- \`models/\`: Directory containing the \`HttpError\` model used for custom error handling.
- \`uploads/\`: Directory where uploaded images are stored.
- \`public/\`: Directory for serving static files.
- \`package.json\`: Configuration file that includes project dependencies and scripts.
- \`README.md\`: Documentation file (this file).

## Prerequisites

Before running the application, make sure you have the following installed:

- Node.js (version >= 10.x)
- MongoDB

## Getting Started

1. Clone the repository:

```bash
git clone https://github.com/AkhtarShadab/MerN1
```

2. Install dependencies:

```bash
cd MerN1
npm install
```

3. Configure MongoDB:

   - Open the \`app.js\` file and locate the following line:

   ```javascript
   mongoose.connect(
   \`mongodb+srv://<USERNAME>:<PASSWORD>@<CLUTER_NAME>.mongodb.net/\${process.env.DB_NAME}?retryWrites=true&w=majority\`
   )
   ```

   - Replace the connection string with your MongoDB connection string.

4. Start the server:

```bash
npm start
```

By default, the server will run on port 5000. You can access the application by navigating to \`http://localhost:5000\` in your web browser.

## Live Demo

The application is live and can be accessed at: [https://travelmemories.onrender.com/](https://travelmemories.onrender.com/)

## API Endpoints

The following API endpoints are available:

### Places Routes

- **GET /api/places**: Retrieve a list of all places.
- **GET /api/places/:placeId**: Retrieve a specific place by ID.
- **GET /api/places/user/:userId**: Retrieve all places belonging to a specific user.
- **POST /api/places**: Create a new place.
- **PATCH /api/places/:placeId**: Update a specific place.
- **DELETE /api/places/:placeId**: Delete a specific place.

### Users Routes

- **GET /api/users**: Retrieve a list of all users.
- **POST /api/users/signup**: Sign up a new user.
- **POST /api/users/login**: Log in an existing user.
- **POST /api/users/:userId/places**: Create a new place for a specific user.

## Error Handling

Errors are handled using a custom \`HttpError\` model. If an error occurs during the request processing, an appropriate error message and status code are returned.

## File Storage

Uploaded images are stored in the \`uploads/images\` directory. The application uses the \`express.static\` middleware to serve these files.

## Contributing

Contributions are welcome! If you find any issues or have suggestions for improvements, please open an issue or submit a pull request in the repository.

When contributing to this repository, please first discuss the change you wish to make by creating a new issue or contacting the project team members via [email](mailto:sakn501@gmail.com).

## Acknowledgements

This project was developed as part of a learning exercise. Thanks to the developers and contributors of the libraries and resources used in this application.
