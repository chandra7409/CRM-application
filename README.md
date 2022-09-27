This is CRM application 

# Tech Stack Knowledge
# as well as Node.js Mongodb,Git ,Mysql,javascript,and REST full API test for Postman application

in this application are use the dependencies

"dependencies": {
    "bcryptjs": "^2.4.3",
    "body-parser": "^1.20.0",
    "dotenv": "^16.0.2",
    "express": "^4.18.1",
    "jsonwebtoken": "^8.5.1",
    "mongoose": "^6.5.4",
    "node-rest-client": "^3.1.1"
    "nodemailer,
    nodemon npx,
    nodemon -global,
    
  }


User creation and operations **
- ** Sign - up ** < br / >
`POST /crm/api/v1/auth/signup` < br / >
Register user with name, userId, email, password and user type. < br / > < br / >
- ** Sign - in ** < br / >
`POST /crm/api/v1/auth/signin` < br / >
User Sign - in using userId and password. < br / > < br / >
- ** Get all users(Query params userType and userStatus supported) ** < br / >
`GET /crm/api/v1/users` < br / >
An admin can get a list of all users.The list can also be filtered by userType and userStatus. < br / > < br / >
- ** Get user by userId ** < br / >
`GET /crm/api/v1/users/:id` < br / >
A user or an admin can get the data of the user by userId. < br / > < br / >
- ** Update user data ** < br / >
`PUT /crm/api/v1/users/:id` < br / >
A user or an admin can update the data of the user by userId. < br / > < br / >
>
**

Tickets creation and operations **
- ** Create new theatre ** < br / >
`POST /crm/api/v1/Tickets` < br / >
A engineeror an admin can create a theatre. < br / > < br / >
- ** Update a theatre ** < br / >
`PUT /crm/api/v1/Tickets/:id` < br / >
Aengineer or an admin can update their theatre. < br / > < br / >
- ** Delete a theatre ** < br / >
`DELETE /crm/api/v1/Tickets/:id` < br / >
Aengineer or an admin can delete their theatre. < br / > < br / >
- ** Get all Tickets ** < br / >
`GET /crm/api/v1/Tickets` < br / >
Any user can get a list of all Tickets < br / > < br / >
- ** Get Single theatre ** < br / >
`GET /crm/api/v1/Tickets/:id` < br / >
Any user can get a single theatre by theatreId < br / > < br / >
- ** Get movies in a theatre ** < br / >
`GET /crm/api/v1/Tickets/:id/Tickets` < br / >
Any user can get Tickets inside a theatre by theatreId < br / > < br / >
- ** Update Tickets in a theatre ** < br / >
`PUT /crm/api/v1/Tickets/:id/Tickets` < br / >
A engineeror an admin can update Tickets inside their theatre by theatreId. < br / > < br / >
>
**
Booking creation and operations **
- ** Create new booking ** < br / >
`POST /crm/api/v1/bookings` < br / >
Any user can create a booking. < br / > < br / >
- ** Update a booking ** < br / >
`PUT /crm/api/v1/bookings/:id` < br / >
Any user can update their booking. < br / > < br / >
- ** Get Single booking ** < br / >
`GET /crm/api/v1/bookings/:id` < br / >
Any user can get a single booking by bookingId < br / > < br / >
- ** Get all bookings ** < br / >
`GET /crm/api/v1/bookings` < br / >
Any user can get a list of all their bookings < br / > < br / >
>
**
Payment creation and operations **
- ** Create new payment ** < br / >
`POST /crm/api/v1/payments` < br / >
Any user can create a payment. < br / > < br / >
- ** Get Single payment ** < br / >
`GET /crm/api/v1/payments/:id` < br / >
Any user can get a single payment by paymentId < br / > < br / >
- ** Get all payments ** < br / >
`GET /crm/api/v1/payments` < br / >
Any user can get a list of all their payments < br / > < br / >



any problem ask query please
engtilakchandra @gmail.com ===
===
=

>
**
User creation and operations **

- ** Sign - up ** < br / >
`POST /mba/api/v1/auth/signup` < br / >
Register user with name, userId, email, password and user type. < br / > < br / >

- ** Sign - in ** < br / >
`POST /mba/api/v1/auth/signin` < br / >
User Sign - in using userId and password. < br / > < br / >

- ** Get all users(Query params userType and userStatus supported) ** < br / >
`GET /crm/api/v1/users` < br / >
An admin can get a list of all users.The list can also be filtered by userType and userStatus. < br / > < br / >

- ** Get user by userId ** < br / >
`GET /crm/api/v1/users/:id` < br / >
A user or an admin can get the data of the user by userId. < br / > < br / >

- ** Update user data ** < br / >
`PUT /crm/api/v1/users/:id` < br / >
A user or an admin can update the data of the user by userId. < br / > < br / >
