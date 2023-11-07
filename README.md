# Notes App Back-End

This is the back-end component of a simple notes app. It provides a set of APIs for creating, retrieving, updating, and deleting notes. The application is built using Node.js and Hapi.js framework.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
- [Linting](#linting)
- [Dependencies](#dependencies)

## Installation

To run the application locally, follow these steps:

1. Clone this repository:

   ```
   git clone <repository-url>
   cd notes-app-back-end
   ```

2. Install the project dependencies:

   ```
   npm install
   ```

3. Start the development server:

   ```
   npm run start-dev
   ```

The server will run on `http://localhost:5000` by default.

## Usage

This back-end server provides a RESTful API for managing notes. You can use any REST client to interact with the API. Here are the available endpoints:

## API Endpoints

- `POST /notes`: Create a new note.
- `GET /notes`: Retrieve a list of all notes.
- `GET /notes/{id}`: Retrieve a specific note by its ID.
- `PUT /notes/{id}`: Update a specific note by its ID.
- `DELETE /notes/{id}`: Delete a specific note by its ID.

### Example Request:

```json
POST /notes
{
  "title": "Sample Note",
  "tags": ["sample", "demo"],
  "body": "This is a sample note."
}
```

### Example Response:

```json
201 Created
{
  "status": "success",
  "message": "Note berhasil dibuat",
  "data": {
    "noteId": "generated-id"
  }
}
```

## Linting

We use ESLint with the AirBnB coding style for linting. You can run linting checks with the following command:

```
npm run lint
```

## Dependencies

- [Hapi](https://hapi.dev/): The web framework used to create the server.
- [Nanoid](https://github.com/ai/nanoid): A small and efficient library for generating unique IDs.
- [Eslint](https://eslint.org/): A linting tool for ensuring code quality.

## License

This project is licensed under the ISC License - see the [LICENSE](LICENSE) file for details.
