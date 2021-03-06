## Introduction to Service Design and Engineering 
## 		Assignment # 2

### GENERAL INFORMATION
In the assignment, I worked alone.  
Server @ https://mysterious-waters-69770.herokuapp.com

### The following are the supported REST endpoints:

##### **GET /person**
- Get all persons

##### **GET /person/{id}**
- Get a person with its id

##### **GET /person/{id}/{measureType}**
- Get all the specified measures from a person specified with id

##### **GET /person/{id}/{measureType}/{mid}**
- Get a single measure specified with measure id, measure type and person id

##### **GET /person?measureType={measureType}&min={min}&max={max}**
- Return all persons that have measure that match [min,max] values

##### **GET /person/{id}/{measureType}?before={beforeDate}&after={afterDate}**
- Return all measures of person specified by id that match the given before and after dates
- date format: YYYY-MM-DD

##### **GET /measureTypes**
- Get all the measure types that are supported

##### **POST /person**
- Create a new person

##### **POST /person/{id}/{measureType}**
- Create a new measure for person specified by id

##### **PUT /person/{id}**
- Update a person specified by id

##### **PUT /person/{id}/{measureType}/{mid}**
- Update a measure specified by measure id, measure type and person id

##### **DELETE /person/{id}**
- Delete a person specified by id

### ABOUT
This assignment is about RESTful services. In the assignment I have created a REST service that is running on Heroku and a client that is making requests to the server.

### STRUCTURE
The root folder contains mainly setup and configuration files and the database file. The src-package consist of all the needed java files for the program in addition with the persistence.xml-file. WebContent-folder contains files for server setup, such as web.xml.

### FILE FUNCTION
The ivy.xml and build.xml files in root folder are for installing all the dependencies and running the program. The lifecoach.sqlite is the database file and app.json and Procfile in root folder contains setups for Heroku. Log-files contains logs from client-server requests.
The src-package contains all the java files and persistence.xml-file for persistence units. The introsde.rest.ehealth-package contains server configuration files, introsde.rest.ehealt.client contains the client, introsde.rest.ehealth.dao contains file for interacting with database, introsde.rest.ehealt.model contains the model files and introsde.rest.ehealth.resources contains the resource-handling -files for the uri paths.

### RUN 
The program uses ant build-tool for running the program. To execute the program, please open the terminal and run the following command in the root directory of the program:

	ant execute.client

The above command installs all dependencies and executes the client. The client sends requests to the remote server running on Heroku and prints the results to the terminal and also saves them to logs in the root folder.	
