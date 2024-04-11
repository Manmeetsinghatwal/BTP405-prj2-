# BTP405 Project 2

- Name: Manmeet Singh Atwal
- E-mail: matwal4@myseneca.ca
- ID: 122872229


## Item Vision: 
To foster a cloud-based eatery reservation framework that smoothes out the most common way of making, making due, and dropping reservations on the web. The framework means to give a consistent encounter to the two clients and eatery staff, offering highlights like ongoing booking accessibility, client data the executives, and robotized reservation notices. 
## Goals: 
- Make it more straightforward for clients to hold tables. - Further develop proficiency for café staff. - Improve generally speaking consumer loyalty. - Guarantee the framework is adaptable, adaptable, and simple to keep up with microservices engineering.
- ## Necessities:
- - Framework for clients to book tables. - Backend framework for staff to deal with appointments and client subtleties. - Mechanized cautions for reservation affirmations and retractions. - Secure login and approval strategies. - Design equipped for dealing with various degrees of interest.
  - ## Ideal interest group:
  - Our objective clients incorporate eatery proprietors, chiefs, and clients who need to book tables on the web.
  -  ## Key Highlights:
  -  - Client account the executives. - Table booking and dropping. - Continuous updates on table accessibility. - The board of client data. - Computerized reservation notices. - Revealing and investigation devices for eatery proprietors.
     - ## Issues Tackled:
     - - Killing blunders and failures in manual booking processes. - Working on the administration of table accessibility and client information. - Giving convenient updates to clients about their reservations. - Further developing correspondence channels for reservation cautions.
     - ## Client Stories:
     - - As a client, I need to effectively make a record to helpfully book tables. - As a client, I need to look for accessible tables in light of date, time, and party size. - As a staff part, I need to see and oversee current table accessibility. - As a staff part, I need to get notices when a booking is made or dropped. - As a client, I need to get email affirmations for my reservations.
     -  ## Situations:
     -  - A client visits the eatery's site, joins, and holds a table utilizing their email. - The client chooses the date, time, and party size, and in a split second sees accessible tables. - When affirmed, the booking is signed in the framework, and the client receives an email affirmation. - If necessary, the client can drop or change their booking through their record. - Café staff get warnings of new reservations and can refresh table accessibility through their connection point.
## Outcomes: 

#### Create a new User

```
POST /user
Content-Type: application/json
{
    "Name": "Rodry James",
    "Email": "rj5@gmail.com"
}
```
#### Outcome
```
Status: 201 Created
{
    "user_id": 1,
    "name": "Rodry James",
    "email": "rj5@gmail.com"
}
```


#### Create a new Reservation:

```
POST /reservation
Content-Type: application/json

{

"user_id": 1,
"reservation_time": "2024-04-6 19:00:00",
"guests": 4,
"status": "Confirmed"
}
```

#### Outcome
```
Status: 201 Created
{
    "message": "Reservation Created Succesfully."
}
```


#### Check Reservations:

```
Status: 200 OK
[
   {
      "reservation_id": 1,
      "user_id": 1,
      "reservation_time": "2024-04-06 19:00:00",
      "guests": 4,
      "status": "Confirmed"

   }
]
```
#### Update Reservation:

```
PUT /reservation/{reservation_id}
Content-Type: application/json
[
   {
      "reservation_time": "2024-04-09 21:00:00",
      "guests": 8,
      "status": "Confirmed"

   }
]

```
#### Outcome
```
Status: 201 Created
{
    "message": "Reservation Updated Succesfully."
}
```

#### Delete Reservation:

```
DELETE /reservation/{reservation_id}
Status: 200 Ok
{
    "message": "Reservation Deleted Succesfully."
}
```
