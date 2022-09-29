Tech Stack Knowledge
as well as Node.js Mongodb, Git, Mysql, javascript, and REST full API test
for Postman application

    in this application are use the dependencies

    "dependencies": {
    "bcryptjs": "^2.4.3",
    "body-parser": "^1.20.0",
    "dotenv": "^16.0.2",
    "express": "^4.18.1",
    "jsonwebtoken": "^8.5.1",
    "mongoose": "^6.5.4",
    "node-rest-client": "^3.1.1"
    "nodemailer, nodemon npx, nodemon -global,

}

Learning the development of RESTful APIs
for backend

This code base contains logic / structure
for creating the Restful APIs
for the CRM app Features

User Registration and User Login
Customer Activites
Engineer 's activities
Adming activities
Unit testing

More details around this can be found here How is the code organized in this repo ?

    The whole repo is divided into multiple branches.Each branch contains code
for a specific concept.For example session1 has the code base
for user registration and login.Each branch is built on the top of the previous branch Prerequisite

Understanding of Node.js
Understanding of Async Await
Mongo DB locally installed and running

his code base contains logic / structure
for creating the Restful APIs
for the CRM app
Features

More details around this can be found here
Prerequisite

Understanding of Node.js
Understanding of Async Await
Mongo DB locally installed and running
JWT tokens

Tech

Node.js
Mongodb

Installation

this app requires Node.js v14 + to run.

Install the dependencies and devDependencies and start the server.

Before starting the server please ensure mongodb server is locally installed and running on the
default port

cd CRM - Application--FSD - Bootcamp
npm install
npm run devStart

Rest endpoints
1. Sign Up request

POST / crm / api / v1 / auth / signup
Sample request body: {
    "name": "Tilak",
    "userId": "Asus1212",
    "email": "abc@xyz.com",
    "password": "Welcome1",
    "userType": "ENGINEER"
}

Sample response body: {
    "name": "Tilak",
    "userId": "Asus1212",
    "email": "abc@xyz.com",
    "userTypes": "ENGINEER",
    "userStatus": "PENDING",
    "createdAt": "2022-02-20T04:47:43.842Z",
    "updatedAt": "2022-02-20T04:47:43.842Z"
}

Details about the JSON structure

name: Mandatory
userId: Manadatory + Unique
email: Manadatory + Unique
passworod: Mandatory
userType: Optional,
    default value is CUSTOMER.Other possible value: ADMIN | ENGINEER
userStatus: It reperesents the status of the user registered.Customer are by
default approved.ADMIN and Engineers need approval from Admin.Possible values: APPROVED | PENDING | REJECTED

2. Login request

POST / crm / api / v1 / auth / signin
Sample request body: {
    "userId": "Asus7409",
    "password": "Welcome1"

}
Sample response body: {
    "name": "Tilak",
    "userId": "Asus7409",
    "email": "abc@xyz1.com",
    "userTypes": "CUSTOMER",
    "userStatus": "APPROVED",
    "accessToken": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IlZpc2gwMSIsImlhdCI6MTY0NTMzMjg3NiwiZXhwIjoxNjQ1NDE5Mjc2fQ.21IRt9VIL-suvP7Z_lamH1PcchOB1TJOhZPSpX9kqt8"
}

3. Get all users

GET / crm / api / v1 / users /
    Headers:
    Content - Type: application / json
x - access - token: eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6ImFkbWluIiwiaWF0IjoxNjQ1NTA4NDY0LCJleHAiOjE2NDU1OTQ4NjR9.PgKiGRN_J8aDGwrBLOGhWUKArcfegDd76dEgGtV6Qh0
Sample request body:


    Sample response body: [{
            "name": "Tilak",
            "userId": "admin",
            "email": "engtilakchandra@gmail.com",
            "userTypes": "ADMIN",
            "userStatus": "APPROVED"
        },
        {
            "name": "Tilak",
            "userId": "Asus7409",
            "email": "abc@xyz1.com",
            "userTypes": "ENGINEER",
            "userStatus": "APPROVED"
        },
        {
            "name": "chnadra",
            "userId": "chnadra7409",
            "email": "abc@mohan.com",
            "userTypes": "CUSTOMER",
            "userStatus": "APPROVED"
        }
    ]

Details about the JSON structure

name: Mandatory
userId: Manadatory + Unique
email: Manadatory + Unique
passworod: Mandatory
userType: Optional,
    default value is CUSTOMER.Other possible value: ADMIN | ENGINEER
userStatus: It reperesents the status of the user registered.Customer are by
default approved.ADMIN and Engineers need approval from Admin.Possible values: APPROVED | PENDING | REJECTED

4. Get user based on the userId

GET / crm / api / v1 / users / { userId }

Headers:
    Content - Type: application / json
x - access - token: eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6ImFkbWluIiwiaWF0IjoxNjQ1NTA4NDY0LCJleHAiOjE2NDU1OTQ4NjR9.PgKiGRN_J8aDGwrBLOGhWUKArcfegDd76dEgGtV6Qh0


Sample response body: [{
    "name": "Tilak",
    "userId": "Asus7409",
    "email": "abc@xyz1.com",
    "userTypes": "ENGINEER",
    "userStatus": "APPROVED"
}]

5. Update the user information - Type and Status

PUT localhost: 8080 / crm / api / v1 / users / Asus7409

Headers:
    Content - Type: application / json
x - access - token: eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6ImFkbWluIiwiaWF0IjoxNjQ1NTA4NDY0LCJleHAiOjE2NDU1OTQ4NjR9.PgKiGRN_J8aDGwrBLOGhWUKArcfegDd76dEgGtV6Qh0


Sample request body: {
    "name": "Tilak",
    "userId": "Asus7409",
    "email": "abc@xyz1.com",
    "userTypes": "ENGINEER",
    "userStatus": "APPROVED"
}

Sample response body: {
    "message": "User record has been updated successfully"
}

6. Create a new ticket

POST / crm / api / v1 / tickets /
    Headers:
    Content - Type: application / json
x - access - token: eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6ImFkbWluIiwiaWF0IjoxNjQ1NTA4NDY0LCJleHAiOjE2NDU1OTQ4NjR9.PgKiGRN_J8aDGwrBLOGhWUKArcfegDd76dEgGtV6Qh0
Sample request body: {
    "title": "Not able to use the device",
    "description": "Device is not turning on with power"
}

Sample response body: {
    "title": "Not able to use the device",
    "ticketPriority": 4,
    "description": "Device is not turning on with power",
    "status": "OPEN",
    "reporter": "Asus7409",
    "assignee": "Asus1212",
    "id": "6215d8288d78a94e0a5a0610",
    "createdAt": "2022-02-23T06:46:00.414Z",
    "updatedAt": "2022-02-23T06:46:00.414Z"
}

7. Get all tickets

GET / crm / api / v1 / tickets /

    Headers:
    Content - Type: application / json
x - access - token: eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6ImFkbWluIiwiaWF0IjoxNjQ1NTA4NDY0LCJleHAiOjE2NDU1OTQ4NjR9.PgKiGRN_J8aDGwrBLOGhWUKArcfegDd76dEgGtV6Qh0


Sample response body: [{
        "title": "Not Able to update",
        "ticketPriority": 4,
        "description": "Update functionality is not working for my device",
        "status": "OPEN",
        "reporter": "Asus7409",
        "assignee": "Asus1212",
        "id": "6215c1e85e0d5a53afcd4e68",
        "createdAt": "2022-02-23T05:11:04.841Z",
        "updatedAt": "2022-02-23T05:11:04.841Z"
    },
    {
        "title": "Not able to use the device",
        "ticketPriority": 4,
        "description": "Device is not turning on with power yessss",
        "status": "CLOSED",
        "reporter": "Asus7409",
        "assignee": "Asus1212",
        "id": "6215ceb86ba4fcbac9433282",
        "createdAt": "2022-02-23T06:05:44.352Z",
        "updatedAt": "2022-02-23T06:05:44.353Z"
    },
    {
        "title": "Not able to use the device",
        "ticketPriority": 4,
        "description": "Device is not turning on with power",
        "status": "OPEN",
        "reporter": "Asus7409",
        "assignee": "Asus1212",
        "id": "6215d8288d78a94e0a5a0610",
        "createdAt": "2022-02-23T06:46:00.414Z",
        "updatedAt": "2022-02-23T06:46:00.414Z"
    }
]

8. Get all tickets fitered by status

GET / crm / api / v1 / tickets ? status = OPEN

Headers:
    Content - Type: application / json
x - access - token: eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6ImFkbWluIiwiaWF0IjoxNjQ1NTA4NDY0LCJleHAiOjE2NDU1OTQ4NjR9.PgKiGRN_J8aDGwrBLOGhWUKArcfegDd76dEgGtV6Qh0
Response: [{
        "title": "Not Able to update",
        "ticketPriority": 4,
        "description": "Update functionality is not working for my device",
        "status": "OPEN",
        "reporter": "Asus7409",
        "assignee": "Asus1212",
        "id": "6215c1e85e0d5a53afcd4e68",
        "createdAt": "2022-02-23T05:11:04.841Z",
        "updatedAt": "2022-02-23T05:11:04.841Z"
    },
    {
        "title": "Not able to use the device",
        "ticketPriority": 4,
        "description": "Device is not turning on with power",
        "status": "OPEN",
        "reporter": "Asus7409",
        "assignee": "Asus1212",
        "id": "6215d8288d78a94e0a5a0610",
        "createdAt": "2022-02-23T06:46:00.414Z",
        "updatedAt": "2022-02-23T06:46:00.414Z"
    }
]

9. Update the given ticket(Only the creator of the ticket should be able to update it)

PUT / crm / api / v1 / tickets / 6215 c1e85e0d5a53afcd4e68

Headers:
    Content - Type: application / json
x - access - token: eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6ImFkbWluIiwiaWF0IjoxNjQ1NTA4NDY0LCJleHAiOjE2NDU1OTQ4NjR9.PgKiGRN_J8aDGwrBLOGhWUKArcfegDd76dEgGtV6Qh0

Request body: {
    "title": "Not Able to update",
    "ticketPriority": 4,
    "description": "Update functionality is not working for my device",
    "status": "CLOSED"

}

Response body: {
    "title": "Not Able to update",
    "ticketPriority": 4,
    "description": "Update functionality is not working for my device",
    "status": "CLOSED",
    "reporter": "Asus7409",
    "assignee": "Asus1212",
    "id": "6215c1e85e0d5a53afcd4e68",
    "createdAt": "2022-02-23T05:11:04.841Z",
    "updatedAt": "2022-02-23T05:11:04.841Z"
}

10. Get the ticket based on the ticket id

GET / crm / api / v1 / tickets / { id }

Headers:
    Content - Type: application / json
x - access - token: eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6ImFkbWluIiwiaWF0IjoxNjQ1NTA4NDY0LCJleHAiOjE2NDU1OTQ4NjR9.PgKiGRN_J8aDGwrBLOGhWUKArcfegDd76dEgGtV6Qh0
Response: {
    "title": "Not Able to update",
    "ticketPriority": 4,
    "description": "Update functionality is not working for my device",
    "status": "OPEN",
    "reporter": "Asus7409",
    "assignee": "Asus1212",
    "id": "6215c1e85e0d5a53afcd4e68",
    "createdAt": "2022-02-23T05:11:04.841Z",
    "updatedAt": "2022-02-23T05:11:04.841Z"
}

11. API
for authenticated Engineer to be able to see the complete list of tickets assigned to him / her

GET / crm / api / v1 / tickets /
    Headers:
    Content - Type: application / json
x - access - token: eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6ImFkbWluIiwiaWF0IjoxNjQ1NTA4NDY0LCJleHAiOjE2NDU1OTQ4NjR9.PgKiGRN_J8aDGwrBLOGhWUKArcfegDd76dEgGtV6Qh0

Sample response body: [{
        "title": "Not Able to update",
        "ticketPriority": 4,
        "description": "Update functionality is not working for my device",
        "status": "CLOSED",
        "reporter": "Asus7409",
        "assignee": "Asus1212",
        "id": "6215c1e85e0d5a53afcd4e68",
        "createdAt": "2022-02-23T05:11:04.841Z",
        "updatedAt": "2022-02-23T05:11:04.841Z"
    },
    {
        "title": "Not able to use the device",
        "ticketPriority": 4,
        "description": "Device is not turning on with power yessss",
        "status": "CLOSED",
        "reporter": "Asus7409",
        "assignee": "Asus1212",
        "id": "6215ceb86ba4fcbac9433282",
        "createdAt": "2022-02-23T06:05:44.352Z",
        "updatedAt": "2022-02-23T06:05:44.353Z"
    },
    {
        "title": "Not able to use the device",
        "ticketPriority": 4,
        "description": "Device is not turning on with power",
        "status": "OPEN",
        "reporter": "Asus7409",
        "assignee": "Asus1212",
        "id": "6215d8288d78a94e0a5a0610",
        "createdAt": "2022-02-23T06:46:00.414Z",
        "updatedAt": "2022-02-23T06:46:00.414Z"
    }
]

12. API
for authenticated Engineer to search
for the ticket

GET / crm / api / v1 / tickets / { id }

Headers:
    Content - Type: application / json
x - access - token: eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6ImFkbWluIiwiaWF0IjoxNjQ1NTA4NDY0LCJleHAiOjE2NDU1OTQ4NjR9.PgKiGRN_J8aDGwrBLOGhWUKArcfegDd76dEgGtV6Qh0


Sample response body: {
    "title": "Not Able to update",
    "ticketPriority": 4,
    "description": "Update functionality is not working for my device",
    "status": "CLOSED",
    "reporter": "Asus7409",
    "assignee": "Asus1212",
    "id": "6215c1e85e0d5a53afcd4e68",
    "createdAt": "2022-02-23T05:11:04.841Z",
    "updatedAt": "2022-02-23T05:11:04.841Z"
}

13. API
for the authenticated Engineer to update the ticket / reassign the ticket assigned to him / her

PUT / crm / api / v1 / tickets / 6215 c1e85e0d5a53afcd4e68

Headers:
    Content - Type: application / json
x - access - token: eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6ImFkbWluIiwiaWF0IjoxNjQ1NTA4NDY0LCJleHAiOjE2NDU1OTQ4NjR9.PgKiGRN_J8aDGwrBLOGhWUKArcfegDd76dEgGtV6Qh0

Request: {
    "title": "Not Able to update",
    "ticketPriority": 4,
    "description": "Update functionality is not working for my device",
    "status": "CLOSED",
    "reporter": "Asus7409",
    "assignee": "Shiv01",
    "id": "6215c1e85e0d5a53afcd4e68"

}
Response: {
    "title": "Not Able to update",
    "ticketPriority": 4,
    "description": "Update functionality is not working for my device",
    "status": "CLOSED",
    "reporter": "Asus7409",
    "assignee": "Shiv01",
    "id": "6215c1e85e0d5a53afcd4e68",
    "createdAt": "2022-02-23T05:11:04.841Z",
    "updatedAt": "2022-02-23T05:11:04.841Z"
}

14. API
for the authenticated ADMIN to get the list of all the issues

GET / crm / api / v1 / tickets /

    Headers:
    Content - Type: application / json
x - access - token: eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6ImFkbWluIiwiaWF0IjoxNjQ1NTA4NDY0LCJleHAiOjE2NDU1OTQ4NjR9.PgKiGRN_J8aDGwrBLOGhWUKArcfegDd76dEgGtV6Qh0



Response body: [{
        "title": "Not Able to update",
        "ticketPriority": 4,
        "description": "Update functionality is not working for my device",
        "status": "CLOSED",
        "reporter": "Asus7409",
        "assignee": "Shiv01",
        "id": "6215c1e85e0d5a53afcd4e68",
        "createdAt": "2022-02-23T05:11:04.841Z",
        "updatedAt": "2022-02-23T05:11:04.841Z"
    },
    {
        "title": "Not able to use the device",
        "ticketPriority": 4,
        "description": "Device is not turning on with power yessss",
        "status": "CLOSED",
        "reporter": "Asus7409",
        "assignee": "Asus1212",
        "id": "6215ceb86ba4fcbac9433282",
        "createdAt": "2022-02-23T06:05:44.352Z",
        "updatedAt": "2022-02-23T06:05:44.353Z"
    },
    {
        "title": "Not able to use the device",
        "ticketPriority": 4,
        "description": "Device is not turning on with power",
        "status": "OPEN",
        "reporter": "Asus7409",
        "assignee": "Asus1212",
        "id": "6215d8288d78a94e0a5a0610",
        "createdAt": "2022-02-23T06:46:00.414Z",
        "updatedAt": "2022-02-23T06:46:00.414Z"
    },
    {
        "title": "Not able to use the device again",
        "ticketPriority": 4,
        "description": "Device is not turning on with power",
        "status": "OPEN",
        "reporter": "Asus7409",
        "assignee": "Asus1212",
        "id": "62270ca27db35f99978ac346",
        "createdAt": "2022-03-08T07:58:26.362Z",
        "updatedAt": "2022-03-08T07:58:26.362Z"
    },
    {
        "title": "Not able to use the device again",
        "ticketPriority": 4,
        "description": "Device is not turning on with power",
        "status": "OPEN",
        "reporter": "Vish02",
        "assignee": "Asus1212",
        "id": "6227127436d167dde19c2a3b",
        "createdAt": "2022-03-08T08:23:16.902Z",
        "updatedAt": "2022-03-08T08:23:16.903Z"
    }
]

15. API
for the authenticated ADMIN to get the list of all the issues based on filters

GET / crm / api / v1 / tickets ? status = OPEN

Headers:
    Content - Type: application / json
x - access - token: eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6ImFkbWluIiwiaWF0IjoxNjQ1NTA4NDY0LCJleHAiOjE2NDU1OTQ4NjR9.PgKiGRN_J8aDGwrBLOGhWUKArcfegDd76dEgGtV6Qh0
Response: [{
        "title": "Not able to use the device",
        "ticketPriority": 4,
        "description": "Device is not turning on with power",
        "status": "OPEN",
        "reporter": "Asus7409",
        "assignee": "Asus1212",
        "id": "6215d8288d78a94e0a5a0610",
        "createdAt": "2022-02-23T06:46:00.414Z",
        "updatedAt": "2022-02-23T06:46:00.414Z"
    },
    {
        "title": "Not able to use the device again",
        "ticketPriority": 4,
        "description": "Device is not turning on with power",
        "status": "OPEN",
        "reporter": "Asus7409",
        "assignee": "Asus1212",
        "id": "62270ca27db35f99978ac346",
        "createdAt": "2022-03-08T07:58:26.362Z",
        "updatedAt": "2022-03-08T07:58:26.362Z"
    },
    {
        "title": "Not able to use the device again",
        "ticketPriority": 4,
        "description": "Device is not turning on with power",
        "status": "OPEN",
        "reporter": "Vish02",
        "assignee": "Asus1212",
        "id": "6227127436d167dde19c2a3b",
        "createdAt": "2022-03-08T08:23:16.902Z",
        "updatedAt": "2022-03-08T08:23:16.903Z"
    }
]
