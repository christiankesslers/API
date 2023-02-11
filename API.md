
# MoonbaseDAO API V1 Documentation

  

# contacts

  

## api/v1/contacts: GET endpoint for retrieving a list of all contacts.


+ ###  Sample Request:

    
   

    GET /api/v1/contacts



+ ### Sample Response:

  

    {“id”: 1,  
“first_name”: “John”,  
“last_name”: “Doe”,  
“email”:  ["johndoe@example.com](mailto:%22johndoe@example.com)",  
“phone_number”: “1234567890”,  
“address”: “123 Main St.”,  
“city”: “Anytown”,  
“state”: “CA”,  
“zip_code”: “12345”,  
“created_at”: “2022-01-01T12:00:00Z”,  
“updated_at”: “2022-01-01T12:00:00Z”},  
{“id”: 2,  
“first_name”: “Jane”,  
“last_name”: “Doe”,  
“email”:  ["janedoe@example.com](mailto:%22janedoe@example.com)",  
“phone_number”: “0987654321”,  
“address”: “456 Elm St.”,  
“city”: “Anytown”,  
“state”: “CA”,  
“zip_code”: “67890”,  
“created_at”: “2022-01-02T12:00:00Z”,  
“updated_at”: “2022-01-02T12:00:00Z”    
     }  
}


   






   ## api/v1/contacts/{contactId} ': GET endpoint for retrieving a specific contact.

  
  
  
+ ### Sample Request:

    GET /api/v1/contacts/1/

  

+ ### Sample Response

  

    HTTP/1.1 200 OK
    
    Content-Type: application/json
    
      
    
    {
    
    "id": 1,
    "first_name": "John",   
    “last_name": "Doe", 
    "email": "johndoe@example.com",  
    "phone_number": "1234567890",
    "address": "123 Main St.",
    "city": "Anytown",
    "state": "CA",
    "zip_code": "12345",
    "created_at": "2022-01-01T12:00:00Z",
    "updated_at": "2022-01-01T12:00:00Z"
       }
    }
 

   
      
    
##   /api/v1/contacts: POST endpoint for creating a new contact.
    
      
    
 + ###  Sample Request:
    
      
    
   

    POST /api/v1/contacts HTTP/1.1
    Content-Type: application/json
    Authorization: Bearer <token>
    
      
    
    {“first_name": "John",
         "last_name": "Doe",
    "email": "johndoe@example.com",
    "phone": "+123456789",
    "address": "123 Main St, Anytown USA 12345",
    "notes": "Important contact"
    }
    }
      
    
  
    
    

  

+ ### Sample Response:

      
    
    'HTTP/1.1 201 Created
    Content-Type: application/json
    
      
    
    {
    "id": 123,
    "first_name": "John",
    "last_name": "Doe",
    "email": "johndoe@example.com",
    "phone": "+123456789",
    "address": "123 Main St, Anytown USA 12345",
    "notes": "Important contact",
    "created_at": "2022-12-01T12:00:00Z",
    "updated_at": "2022-12-01T12:00:00Z    
    }
    }
    
     

  

## /api/v1/contacts/{contactId}: PUT endpoint for updating an existing contact.

  
  

+ ### Sample Request:

  

 

       'PUT /api/v1/contacts/123 HTTP/1.1
    Content-Type: application/json
    Authorization: Bearer <token>
   
    
    {
    "first_name": "Jane",
    
    "last_name": "Doe",
    
    "email": "janedoe@example.com",
    
    "phone": "+987654321",
    
    "address": "456 Main St, Anytown USA 65432",
    
    "notes": "Important client"
    
    }'

+ ### Sample Response:

 

     
    
    'HTTP/1.1 200 OK
    
    Content-Type: application/json
    
      
    
    {
    
    "id": 123,
    
    "first_name": "Jane",
    
    "last_name": "Doe",
    
    "email": "janedoe@example.com",
    
    "phone": "+987654321",
    
    "address": "456 Main St, Anytown USA 65432",
    
    "notes": "Important client",
    
    "created_at": "2022-12-01T12:00:00Z",
    
    "updated_at": "2022-12-02T12:00:00Z"
    
    }'
    
      


  

+ ## //api/v1/contacts/{contactId}: DELETE endpoint for deleting a contact.

  

Sample Request:

  

    DELETE /api/v1/contacts/123 
 
 
    HTTP/1.1
    
    Authorization: Bearer <token>

  

Sample Response:

  

    'HTTP 200 OK
    
    Content-Type: application/json
    
      
    
    {
    
    "message": "Contact with id: {contactId} successfully deleted"
    
    }'
    
      
      

  

---

  

/api/v1/contacts/list: GET endpoint for returning a list view of all contacts.

  
  
  

Sample Request:

  

    'GET /api/v1/contacts/list
    
    Content-Type: application/json
    
    Authorization: Bearer <Access  Token>

Sample Response:

    'HTTP 200 OK
    
    Content-Type: application/json
    
      
    
    [
    
    {
    
    "id": 1,
    
    "name": "John Doe",
    
    "email": "john.doe@example.com",
    
    "phone": "555-555-5555",
    
    "created_at": "2022-06-01T12:00:00.000000Z",
    
    "updated_at": "2022-06-01T12:00:00.000000Z"
    
    },
    
    {
    
    "id": 2,
    
    "name": "Jane Doe",
    
    "email": "jane.doe@example.com",
    
    "phone": "555-555-5556",
    
    "created_at": "2022-06-02T12:00:00.000000Z",
    
    "updated_at": "2022-06-02T12:00:00.000000Z"
    
    }
    
    ]'

  

---

  

/api/v1/contacts/kanban: GET endpoint for returning a kanban view of all contacts.

  

Sample Request:

  

    'GET /api/v1/contacts/kanban
    
    Content-Type: application/json
    
    Authorization: Bearer <Access  Token>

'

  

Sample Response:

      
    
    'HTTP 200 OK
    
    Content-Type: application/json
    
      
    
    [
    
    {
    
    "id": 1,
    
    "name": "John Doe",
    
    "email": "john.doe@example.com",
    
    "phone": "555-555-5555",
    
    "created_at": "2022-06-01T12:00:00.000000Z",
    
    "updated_at": "2022-06-01T12:00:00.000000Z"
    
    },
    
    {
    
    "id": 2,
    
    "name": "Jane Doe",
    
    "email": "jane.doe@example.com",
    
    "phone": "555-555-5556",
    
    "created_at": "2022-06-02T12:00:00.000000Z",
    
    "updated_at": "2022-06-02T12:00:00.000000Z"
    
    }
    
    ]'

  
  

---

  

/api/v1/contacts/gantt: GET endpoint for returning a gannt view of all contacts.

  

Sample Request:

  

    'GET /api/v1/contacts/gantt
    
    Authorization: Bearer <ACCESS_TOKEN>'

 
  

Sample Response:

    200 OK
    
      
    
    {
    
    "data": [
    
    {
    
    "id": 1,
    
    "name": "John Doe",
    
    "start_date": "2022-01-01",
    
    "end_date": "2022-01-05"
    
    },
    
    {
    
    "id": 2,
    
    "name": "Jane Doe",
    
    "start_date": "2022-01-02",
    
    "end_date": "2022-01-08"
    
    },
    
    {
    
    "id": 3,
    
    "name": "Jim Smith",
    
    "start_date": "2022-01-03",
    
    "end_date": "2022-01-06"
    
    }
    
    ]
    
    }'

  ## Authentication
  
  #### POST /api/v1/auth/login:

Sample Request:

    {
        "username": "exampleuser",
        "password": "password123"
    }

  

Sample Response:

Success:

      HTTP/1.1 200 OK
    {
        "access_token": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJleHAiOjE1NjUyODgxMDAsImlhdCI6MTU2NTI4NDUwMCwiZW1haWwiOiJleGFtcGxlQGV4YW1wbGUuY29tIiwidXNlcm5hbWUiOiJleGFtcGxldXNlciJ9.T9XrMtOsyFxEq3tBA0hgAn-OobZDmvZ2f_Gmj0XhIm0",
        "expires_in": 3600,
        "refresh_token": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJleHAiOjE1NjUyODgxMDAsImlhdCI6MTU2NTI4NDUwMCwiZW1haWwiOiJleGFtcGxlQGV4YW1wbGUuY29tIiwidXNlcm5hbWUiOiJleGFtcGxldXNlciJ9.T9XrMtOsyFxEq3tBA0hgAn-OobZDmvZ2f_Gmj0XhIm0",
        "token_type": "Bearer"
    }
Failure:

    HTTP/1.1 400 Bad Request
    {
        "error": "Invalid credentials"
    }
    
      
---

## POST /api/v1/auth/logout
  

Sample Request:

            {   
            "access_token": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJleHAiOjE1NjUyODgxMDAsImhdCI6MTU2NTI4NDUwMCwiZW1haWwiOiJleGFtcGxlQGV4YW1wbGUuY29tIiwidXNlcm5hbWUiOiJleGFtcGxldXNlciJ9.T9XrMtOsyFxEq3tBA0hgAn-OobZDmvZ2f_Gmj0XhIm0"
       }

  

Sample Response:
Success:

    HTTP/1.1 200 OK
    {
        "message": "Successfully logged out"
    }
    
   
   Failure:
   

    HTTP/1.1 400 Bad Request
    {
        "error": "Invalid access token"
    }

----  

## /api/v1/auth/register: POST endpoint for registering a new account.

Sample Request:

    {
      "email": "user@example.com",
      "password": "password",
      "first_name": "John",
      "last_name": "Doe"
    }

  

Sample Response:

- succeed

HTTP/1.1 201 Created
{
  "status": "success",
  "message": "User successfully registered."
}

- fail


    HTTP/1.1 400 Bad Request
    {
      "status": "error",
      "message": "Email already exists."
    }

----

## /api/v1/auth/forgot-password: POST endpoint for resetting a forgotten password.

Sample Request:

      {
      "email": "user@example.com"
    }

Sample Response:
- 

    HTTP/1.1 200 OK
    {
      "status": "success",
      "message": "Password reset instructions sent to email."
    }
-

    HTTP/1.1 400 Bad Request
    {
      "status": "error",
      "message": "Email does not exist."
    }


# events

### List all events: GET /api/v1/events
Sample Request:

    GET /api/v1/events HTTP/1.1
    Host: example.com
    Authorization: Bearer <access_token>
    
      

Sample Response:

    HTTP/1.1 200 OK
    Content-Type: application/json
    
    [
      {
        "id": 1,
        "title": "Conference",
        "start_date": "2022-05-01T00:00:00Z",
        "end_date": "2022-05-03T23:59:59Z",
        "location": "New York, NY",
        "details": "The annual conference for the industry leaders."
      },
      {
        "id": 2,
        "title": "Workshop",
        "start_date": "2022-06-01T00:00:00Z",
        "end_date": "2022-06-02T23:59:59Z",
        "location": "San Francisco, CA",
        "details": "A workshop on the latest technologies in the field."
      }
    ]

----
### Get a specific event: GET /api/v1/events/{eventId}


Sample Request:

    GET /api/v1/events/1 
    HTTP/1.1
    Host: example.com
    Authorization: Bearer <access_token>
    
      

Sample Response:

    HTTP/1.1 200 OK
    Content-Type: application/json
    
    {
      "id": 1,
      "title": "Conference",
      "start_date": "2022-05-01T00:00:00Z",
      "end_date": "2022-05-03T23:59:59Z",
      "location": "New York, NY",
      "details": "The annual conference for the industry leaders."
    }

----  
## Update Event PUT /api/v1/events/{eventId}

Sample Request:

    Content-Type: application/json
    Authorization: Bearer {access_token}
    {
        "name": "Event Update",
        "description": "Event Description Update",
        "start_date": "2023-03-01T10:00:00.000Z",
        "end_date": "2023-03-01T12:00:00.000Z",
        "location": "Event Location Update",
        "attendees": [
            {
                "email": "john.doe@example.com",
                "name": "John Doe"
            },
            {
                "email": "jane.doe@example.com",
                "name": "Jane Doe"
            }
        ]
    }

 

Sample Response:

    {
        "id": "2",
        "name": "Event Update",
        "description": "Event Description Update",
        "start_date": "2023-03-01T10:00:00.000Z",
        "end_date": "2023-03-01T12:00:00.000Z",
        "location": "Event Location Update",
        "attendees": [
            {
                "email": "john.doe@example.com",
                "name": "John Doe"
            },
            {
                "email": "jane.doe@example.com",
                "name": "Jane Doe"
            }
        ]
    }

----
### Delete an event
Sample Request:
DELETE /api/v1/events/{eventId}

      Content-Type: application/json
    Authorization: Bearer {access_token}
    #### 204 No Content

The event has been deleted successfully and there is no response body.

Sample Response:

----  
### view in list mode

Sample Request:

    Content-Type: application/json
    Authorization: Bearer {access_token}
    GET /api/v1/events/list

 

Sample Response:

    HTTP/1.1 200 OK
    Content-Type: application/json
    
    [
      {
        "id": 1,
        "name": "Company Retreat",
        "start_date": "2022-12-01",
        "end_date": "2022-12-03",
        "location": "Lake Tahoe, CA",
        "description": "Annual company retreat for team building and strategic planning."
      },
      {
        "id": 2,
        "name": "Holiday Party",
        "start_date": "2022-12-15",
        "end_date": "2022-12-15",
        "location": "Office",
        "description": "End of the year holiday party to celebrate our accomplishments."
      },
    ]

----
Sample Request:

  

Sample Response:

----  

Sample Request:

  

Sample Response:

----
Sample Request:

  

Sample Response:

----  

Sample Request:

  

Sample Response:

----



















