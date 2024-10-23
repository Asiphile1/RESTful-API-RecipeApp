# Recipe App RESTful API

## Project Overview

This API allows users to manage recipes, including creating, updating, deleting, and retrieving recipes. It also supports pagination for efficient handling of large datasets.

### Technologies

- Node.js
- Express.js
- MongoDB
- Mongoose
- dotenv
- body-parser

### API Endpoints

- `POST /api/recipes`: Create a new recipe
- `GET /api/recipes`: Retrieve all recipes (supports pagination)
  - Query params: `page` (default: 1), `pageSize` (default: 10)
- `GET /api/recipes/:id`: Retrieve a specific recipe by ID
- `PUT /api/recipes/:id`: Update a recipe by ID
- `DELETE /api/recipes/:id`: Delete a recipe by ID

### Setup

1. Clone the repository:
   ```bash
   git clone <repository-url>
   ```

2. Install dependencies:

```bash

npm install
```

3. Create a .env file in the root directory with the following content:

```makefile

MONGO_URI=mongodb+srv://<username>:<password>@cluster0.mongodb.net/recipeDB
PORT=5000
```

4. Start the server:

```bash

npm start
```

Testing
Use Postman or Insomnia to test the following API endpoints.

* To add a recipe:

```
{
  "title": "Spaghetti Bolognese",
  "description": "Classic Italian pasta",
  "ingredients": ["spaghetti", "ground beef", "tomato sauce"],
  "steps": ["Boil pasta", "Cook beef", "Mix and serve"]
}
```
