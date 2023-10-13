## API Recelle

The api Recelle is a PHP-based application programming interface designed to manage a database of names. It provides endpoints for creating, retrieving, updating, and deleting name records. The API utilizes the Slim framework for routing and PDO (PHP Data Objects) for secure and efficient database interactions.

## API Description
The API is a powerful tool created in PHP that helps manage a list of names. It has functions to add new names, get existing names, update names, and remove them from the list. It uses Slim framework for easy navigation and PDO (PHP Data Objects) for safe communication with the database.

In essence, this API acts as a bridge between applications and the name database, allowing developers to interact with the data effortlessly. By providing clear and straightforward endpoints, it simplifies the complexities of managing names, making it accessible for developers with various levels of expertise. Whether you're building a small application or a complex system, this API streamlines the process, ensuring that working with name data is efficient, secure, and hassle-free.


## API Endpoints


Insert Data Endpoint (POST /postName)

Description: This endpoint allows you to add a new name to the database.

- Method: POST
- URL: `http://127.0.0.1/api/public/postName`
- Required Parameters:
  - `fname` (string): First name.
  - `lname` (string): Last name.

Retrieve Data Endpoint (GET /printName)

Description: Use this endpoint to retrieve a list of names from the database.

- Method: GET
- URL: `http://127.0.0.1/api/public/printName`

Update Data Endpoint (POST /updateName)

Description: This endpoint enables you to update an existing name record in the database.

- Method: POST
- URL: `http://127.0.0.1/api/public/updateName`
- Required Parameters:
  - `id` (int): The unique identifier of the name.
  - `fname` (string): New first name.
  - `lname` (string): New last name.

Delete Data Endpoint (POST /deleteName)

Description: Use this endpoint to delete a name record from the database.

- Method: POST
- URL: `http://127.0.0.1/api/public/deleteName`
- Required Parameters:
  - `id` (int): The unique identifier of the name to be deleted.

 


## Request Payload

Request payload: 
{
  "lname": "hortizuela",
  "fname": "manny"
}

Request Payload for updateName Endpoint:
{
  "id": 1,
  "lname": "wick",
  "fname": "john"
}
Request Payload for deleteName Endpoint:
{
  "id": 1
}


 


## Response

Response Payload for printName Endpoint
{
  "status": "success",
  "data": [
    {"lname": "hortizuela", "fname": "manny"},
    {"lname": "licayan", "fname": "arnold"}
  ]
}
In the response for the printName endpoint, the status indicates success, and the data field contains an array of objects. Each object represents a name record in the database, including last name (lname) and first name (fname) information for Manny Hortizuela and Arnold Licayan.


 


## Usage

Using Postman to Interact with the API:

1. Insert Data into the Database:
   - Choose the HTTP method as "POST."
   - Input the URL: http://127.0.0.1/api/public/postName.
   - In the request body, provide the parameters "fname" and "lname" with the values you want to insert.
   - Click the "Send" button to execute the request.

2. Update Existing Data:
   - Select the HTTP method as "POST."
   - Enter the URL: http://127.0.0.1/api/public/updateName.
   - Include the parameters "id," "fname," and "lname" in the request body with the updated values.
   - Click "Send" to submit the request.

3. Retrieve Data from the Database:
   - Choose the HTTP method as "GET."
   - Specify the URL: http://127.0.0.1/api/public/printName.
   - Keep the request body empty, as no additional parameters are needed.
   - Click "Send" to retrieve the data.

4. Delete Data from the Database:
   - Set the HTTP method to "POST."
   - Enter the URL: http://127.0.0.1/api/public/deleteName.
   - In the request body, include the "id" parameter with the ID of the data you wish to delete.
   - Click "Send" to initiate the deletion request.


 


## License

No License


 


## Contributors

Edelyn Oliquiano
Recelle Ann Orillada (Collaborator)


 


## Contact
For inquiries or support, please contact:
Recelle Ann Orillada

Email: recelleann.orillada@gmail.com
Phone: 09661730537
