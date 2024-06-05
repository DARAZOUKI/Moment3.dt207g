# Work experiences REST-Web Service

This project implements a RESTful web service for managing work experiences using MongoDB as the database server. 
The web service allows CRUD (Create, Read, Update, Delete) operations to manage work experience records.

## Usage of the Web Service
GET - Retrieve all work experiences

    GET http://localhost:9000/workexperiences
    This endpoint returns all work experiences in JSON format.

POST - Add a new work experience

    POST: http://localhost:9000/workexperiences
    Send a POST request with the following JSON format to add a new work experience:

json

{
  "companyname": "Example Company",
  "jobtitle": "Developer",
  "location": "Stockholm",
  "startdate": "2022-01-01",
  "enddate": "2023-01-01",
  "description": "Responsible for developing and maintaining web applications."
}

PUT - Update a work experience

    PUT: http://localhost:9000/workexperiences/{id}
    Send a PUT request with the work experience ID as part of the URL and the following JSON format to update an existing work experience:

json

{
  "companyname": "New Company",
  "jobtitle": "Lead Developer",
  "location": "Gothenburg",
  "startdate": "2022-01-01",
  "enddate": "2023-01-01",
  "description": "Responsible for leading the development team."
}

DELETE - Delete a work experience

    DELETE: http://localhost:9000/workexperiences/{id}
    Send a DELETE request with the work experience ID as part of the URL to delete a work experience.

## Testing the Web Service

We can test the web service using tools like Postman or by sending HTTP requests with tools like cURL or by writing custom JavaScript clients.

Example with cURL:

    Retrieve all work experiences:

bash

curl http://localhost:9000/workexperiences

    Add a new work experience:

json

curl -X POST -H "Content-Type: application/json" -d '{"companyname":"New Company","jobtitle":"Developer","location":"Stockholm","startdate":"2023-01-01","enddate":"2024-01-01","description":"Responsible for developing new features."}' http://localhost:9000/workexperiences

    Update a work experience:

json

curl -X PUT -H "Content-Type: application/json" -d '{"companyname":"Updated Company","jobtitle":"Lead Developer","location":"Gothenburg","startdate":"2022-01-01","enddate":"2023-01-01","description":"Responsible for leading the development team."}' http://localhost:9000/workexperiences/{id}

    Delete a work experience:

bash

curl -X DELETE http://localhost:9000/workexperiences/{id}

## Conclusion

This web service enables easy management of work experiences with basic CRUD operations. The code is well-commented for easy understanding and maintenance.
