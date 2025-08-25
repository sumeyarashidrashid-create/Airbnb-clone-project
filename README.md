# Airbnb-clone-project
A practice project to build an Airbnb clone for learning back-end development 
##Project Goals 
-Learn and apply software engineering principles 
-Build a scalable web app step by step 
-Implement features like user authenticitication,property listing ,and booking 
##Tech stack 
-*Frontend :*React/Next.js
-**Backend :**Node.js/Express
-Database:**MongoDB/PostgreSQL
-**Version Control:**Git&Github 
##Team Roles
-**Frontend Developer** _ Build the user interface and makes the app responsive 
-**Backend Developer **_Creates APIs, handles logic, connects to database 
-**Database Adminstrator (DBA)**_ Designs and manages the database ,ensures data security 
-**UI/UX Designer** _Creates designs and makes the app user _friendly 
-**Project Manager** _Manages tasks ,deadlines,and communication
-**QA Tester **_ Tests features ,finds bugs ,ensures quality 
## How to Run 
1. Clone the repo
2. Install dependencies ('npm install ')
3. Run the development server ('npm run dev')
   ##Stutus
   Initiall project set up completed
   Team roles defined 
   ##Technology stack
   Here are the main technologies used in this project and their purpose :
   -**React /Next .js**_ used for building the front end (user interface) .Provides interactive pages, reusable components, and responsive design .
   -**Node.js**_Java script routine for building the backend server .Handles request and connects the frontend to the database
   -**Express .js**_A lightweight Node.js framework used to build Restful APIs,manages routes ,and handles business logics.
   -**MongoDB/PostgreSQL**_The Database that stores user data ,property listings,bookings and other important information .MongoDB(NoSQL)is flexible for unstructured data ,while PostgreSQL(SQL) ensures relational data consistency.
   -**Git&Github**_Version control tools for tracking changes ,collaborating and hosting the project code .
Now you can ;
1.Open' README.md 'file .
2. DElete everything inside it .
3. Paste the full content above .
4. Commit changes with a message like; .

#Databaase Design
##Objectives
Understand how the database will be structured for the Airbnb clone project 
##Key Entities 

**Fields:**
-'user _id '(primary key) 
-'name'
'email'
;password _harsh;
'date_joined 

**Notes :**
Auser can own multiple properties .A user can also make multiple bookings 
----
### 2.Properties 
**Fields :**
-'Property_Id"(Primary Key)
-'owner_id'(Foreign key _Users.user_id)
-'title'
-description'
-Location'
**Notes:**
A property belongs to a single user (owner). A property can have a multiple bookings and multiple reviews
----

### 3. Bookings 
**Fields:** 
-'booking _id '(primary Key )
-'property_id'(Foreign key_properties.property_id) 
-'guest _id' (foreign key _users.user_id) 
'start _date'
'end _date 
-'status' 
**Notes:**
A booking belongs to one property and one user (guest).A booking can be linked to a payement .
----
### 4. Reviews 
**Fields:**
-'review_id (primary key ) 
'property_id '(Foreign key_properties.property _id) 
'user_id'(Foreign key_users.user _id) 
'rating
-'comment'
-date_posted

**Notes:**
A review is created by user for a property. A property can have many reviews .
-----
#### 5. Payments 
**Fields:**
_'payment_id '(primary key ) 
- 'booking _id'(Foreign key_Bookings.booking _id )
- -'amounts '
- -'payment dates'
- payment _status'
  **Notes:**
  A payment is always tied to abooking. A booking has exactly one payment record.
  -----
  ### 5. Relationships
  -A **user** can own multiple **properties**
  -A**Property** can have amultiple **Bookings** and **Reviews**
  -A**Booking **belongs to both  a **user(guest)** and a property**
  -A**Review** is created by a **user** for a **Property**
  -A **payemnt** belongs to a **Booking**.
