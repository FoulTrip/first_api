# FastAPI Authors API
This is a simple RESTful API built using FastAPI and MongoDB to manage author details. The API provides endpoints for retrieving, adding, updating, and deleting author information.

# Getting Started
To run the API on your local machine, follow the steps below:

# Prerequisites
 1. Python (version 3.6 or higher) should be installed on your machine.
 2. Install the required Python packages using the following command:
    ```bash
    pip install fastapi uvicorn pymongo passlib
  
# Installation
 1. Clone this repository to your local machine or download the source code as a ZIP file and extract it.
 2. Navigate to the project directory in your terminal or command prompt.

# Running the API
Start the API server:
 - faefwef
   ```bash
   uvicorn main:app --reload
The API will start running on http://127.0.0.1:8000.

# Endpoints
 1. Get all authors
    - URL: /authors
    - Method: GET
    - Response:
      ```json
      [
        {
          "id": "author_id_1",
          "author": "Author Name 1",
          "content": "Author Content 1",
          "source": "Author Source 1"
        },
        {
          "id": "author_id_2",
          "author": "Author Name 2",
          "content": "Author Content 2",
          "source": null
        },
          ...
      ]

 2. Add a new author
    - URL: /authors
    - Method: POST
    - Request Body:
      ```json
      {
        "author": "New Author Name",
        "content": "New Author Content",
        "source": "New Author Source (Optional)"
      }
     - Response:
       ```json
       {
         "id": "new_author_id",
         "author": "New Author Name",
         "content": "New Author Content",
         "source": "New Author Source (Optional)"
       }

 3. Get author by ID
    - URL: /authors/{id}
    - Method: GET
    - Response:
      ```json
      {
         "id": "author_id",
         "author": "Author Name",
         "content": "Author Content",
         "source": "Author Source (Optional)"
      }

 4. Update author by ID
    - URL: /authors/{id}
    - Method: PUT
    - Request Body:
      ```json
      {
        "author": "Updated Author Name",
        "content": "Updated Author Content",
        "source": "Updated Author Source (Optional)"
      }
    - Response:
      ```json
      {
        "id": "author_id",
        "author": "Updated Author Name",
        "content": "Updated Author Content",
        "source": "Updated Author Source (Optional)"
      }

 6. Delete author by ID
    - URL: /authors/{id}
    - Method: DELETE
    - Response Status: 204 No Content
      
# Error Handling
The API handles errors and responds with appropriate messages and status codes when necessary.
