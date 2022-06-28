# MongoDB_Node.js_CRUDP
MongoDB CURD operations and pagination using Node.js API

## API Documentation

#### Books are the documents

### Create a document
  * POST - ``` http://localhost:3000/books/ ```
      #### Headers
        Name: Content-Type
        Value: application/json
      #### Body
      ```JSON
      {
         "title": "The Way of Living",
         "author": "Terry",
         "genres": ["Fantasy", "Magic"],
         "rating": 8,
         "pages": 400,
         "rating": [
            {
                "name": "Yoshi",
                "body": "Great Book!!"
            },
            {
                "name": "John",
                "body": "So so...!"
            }
         ]
      }
      ```

### Display all the documents
  * GET - ``` http://localhost:3000/books/ ```

### Pagination documents
  * GET - ``` http://localhost:3000/books?p=<INTERGER_NUMBER> ```

### Update a document
  * PATCH - ``` http://localhost:3000/books/<OBJECTID_NUMBER> ```
      #### Headers
        Name: Content-Type
        Value: application/json
      #### Body
      ```JSON
      {
        "title": "The Way of Living - 2",
        "author": "Terry 2",
        "genres": ["Fantasy", "Magic", "Drama"],
        "rating": 8.8,
        "pages": 600
      }
      ```

### Delete a document
  * DELETE - ``` http://localhost:3000/books/<OBJECTID_NUMBER> ```
