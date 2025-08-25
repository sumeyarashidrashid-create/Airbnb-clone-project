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

  #API Security
  ##Objectives

  Understand the importance of securing the backend APIs for the Air bnb clone project .

-##Key security Measures 

## 1. Authentication 
**What it is :**Ensures that only registered users can access the system by verifying their identity (E.g.,Using JWT tokens or OAuth).
-**Why it's crucial:**Protects user accouts and sensitive information from unauthorized access 
-----
### 2. Authorized access 
**What it is :88 Determines what actions an authenticated user is allowed to perfom ( eg authenticated user can update their own listings) 
-**Why its crucial:** prevents malicious users from acessing or modifying data they dont own ,ensuring data integrity. 
-----
### 3. Rate limiting & Threat Protection 
-**What it is:** Limits the number of request a client can make in acertain period of time to prevent abuse (eg, brute-force login attempts)
-**Why is this crucial:** Protects the APIs from denial-of-service attack and ensures fair usage of resources .
------
### 4. Data Encryption 
-**What it is:**Encrypts sensitive data during storage and transmission (eg,using HTTPS/TLS and hashed password )
-**Why is it curucial**Protects sensitive information such as user credentials ,personal details, and payment data from being exposed or intercepted 
------

## 5. Secure Payment Handling 
-**What its is :** Ensures all payment transaction are securely processed via trusted third party  providers (eg, stripe, PayPal) 
-**Why its crucial :** Prevents fraud and financial data breaches ,protecting both users and the platforms reputation 
------
## Summary 
API Security is essential for ;
-Protecting **User data ** from leaks and identity theft. 
Securing **Payments** and financial information .
-Maintaining **trust** between the platforms and its users 
-Ensuring **System reliabilitu ** by preventing malicious attacks. 
git commit-m'added security section with the key measures and importance'
git and readme .md 
----

## CI/CD Pipline 
##Objectives 
Understand how CI-Cd (Continous intergration and contious Deployment) Pipline contributes to the development process for the Airbnb clone project 
##What is a CI_CD pipline? 
-**Continous intergration CI :** Every time code is pushed to the repository,it is automatically tested and validated to ensure it intergrates smoothly with the exsisting codebase 
-**Continously DEployment CD:** After code passes testing .it can be automatically deployed to staging or production environment  without manual steps .
##Why is it important ?
-**faster development :**Automates repetetive tasks so developers can focus on building feartures 
-**Improved quality:** Ensures that bugs are caught early through automated testing .
-**Consistency :** Provides reliable and repeatable process for deployments 
- ** Collaboration :** Makes it easier for multiple developers to work on the same project with fewer conflict
- Tools for CI_CD
- -**Github Action :** Automate testing ,building and deployment directly from github.
- **Docker:**Package application into containers for consistent deployments across environments .
- **Jenkins?CircleCI:** Popular CI_CD tools that provide advanced pipline management .
- **AWS/Vercel/Netlify:**For hosting and automating deployments.
  git commit-m 'Added CI-CD Pipline Section with explantion and tools .
  git and readme.md
