# GDINFMG Sample API Server

A Sample API Server for GDINFMG T2 AY2223. Uses Node, Express, and MySQL.

## Project Details

This repository contains the source code for a sample API server programmed in Express and NodeJS, which connects to a local MySQL server. The project contains the following folders:
- [`src/db`](https://github.com/nromblon/gdinfmg-api-server/tree/master/src/db) - contains database-related scripts.
    - [`/db.js`](https://github.com/nromblon/gdinfmg-api-server/blob/master/src/db/db.js) - is a script which contains code that connects to the local SQL server.
    - [`/models`](https://github.com/nromblon/gdinfmg-api-server/tree/master/src/db/models) - contains script(s) which handles CRUD operations on a specific table. Currently, only the model for the `College` relation is implemented.
- [`src/routes/routes.js`](https://github.com/nromblon/gdinfmg-api-server/blob/master/src/routes/routes.js) - contains all of the route handling code for the API server. 
    - *Ideally, route handling should also be separated by domain (e.g., routes/college.js, routes/apply.js, routes/student.js).*
- [`index.js`](https://github.com/nromblon/gdinfmg-api-server/blob/master/index.js) - contains the initialization of the API server. 
- [`admissions_db.sql`](https://github.com/nromblon/gdinfmg-api-server/blob/master/admissions_db.sql) - the SQL script to initialize the database used in the example API server.
- [`GDINFMG.postman_collection.json`](https://github.com/nromblon/gdinfmg-api-server/blob/master/GDINFMG.postman_collection.json) - a [**Postman**](https://www.postman.com/) export file which includes example HTTP requests for every API endpoint featured in this sample API Server.

## Setup & Instructions
1)  Clone the repository either by downloading as ZIP or using git:
```
git clone https://github.com/nromblon/gdinfmg-api-server
```

2)  Reinstall npm dependencies via:
```
npm install
```

3)  Initialize the admissions database in your SQL server using [`admissions_db.sql`](https://github.com/nromblon/gdinfmg-api-server/blob/master/admissions_db.sql)

4)  Create a copy of [`.env.example`](https://github.com/nromblon/gdinfmg-api-server/blob/master/.env.example) and remove the `.example` extension. Modify the values of the environment variables, if necessary (e.g., PORT and SQL_PASSWORD).

5)  Run the node program via:
```
node index
```