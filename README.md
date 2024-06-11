# MongoDB CRUD Operations

This repository contains a simple Node.js application that demonstrates CRUD operations (Create, Read, Update, Delete) using MongoDB.

## Prerequisites

- [Node.js](https://nodejs.org/) installed
- [MongoDB](https://www.mongodb.com/) installed and running

## Setup

1. **Clone the repository:**
    ```sh
    git clone https://github.com/your-username/mongodb-crud.git
    cd mongodb-crud
    ```

2. **Install dependencies:**
    ```sh
    npm install
    ```

3. **Set up MongoDB:**
    - Make sure your MongoDB server is running.
    - Update the MongoDB connection string in `config/database.js`.

## Running the Application

1. **Start the server:**
    ```sh
    node server.js
    ```

2. The server will be running on `http://localhost:3000`.

## API Endpoints

### Create a Student

- **URL:** `/students`
- **Method:** `POST`
- **Body:**
    ```json
    {
        "name": "John Doe",
        "branch": "CS",
        "percentage": 85,
        "gender": "male"
    }
    ```
- **Response:**
    ```json
    {
        "message": "Student created successfully",
        "student": {
            "_id": "60c72b2f9b1e8b3d5c8f5e8f",
            "name": "John Doe",
            "branch": "CS",
            "percentage": 85,
            "gender": "male"
        }
    }
    ```

### Read All Students

- **URL:** `/students`
- **Method:** `GET`
- **Response:**
    ```json
    [
        {
            "_id": "60c72b2f9b1e8b3d5c8f5e8f",
            "name": "John Doe",
            "branch": "CS",
            "percentage": 85,
            "gender": "male"
        },
        ...
    ]
    ```

### Update a Student

- **URL:** `/students/:id`
- **Method:** `PUT`
- **Body:**
    ```json
    {
        "name": "John Smith",
        "branch": "IT",
        "percentage": 90,
        "gender": "male"
    }
    ```
- **Response:**
    ```json
    {
        "message": "Student updated successfully",
        "student": {
            "_id": "60c72b2f9b1e8b3d5c8f5e8f",
            "name": "John Smith",
            "branch": "IT",
            "percentage": 90,
            "gender": "male"
        }
    }
    ```

### Delete a Student

- **URL:** `/students/:id`
- **Method:** `DELETE`
- **Response:**
    ```json
    {
        "message": "Student deleted successfully"
    }
    ```

## Project Structure

