#  QuizApp_With_Microservices
Quiz web application built with Spring Boot, Hibernate, and Swagger that has no user interface and only the model and controller classes that can be tested using the Swagger UI or Postman tool.

######  Tools required: Spring framework, Hibernate, Eclipse IDE, MySQL

------------


Steps to take in order for the application to work properly:

###  Step 1: Configure the database:

-  Access the MySQL server from the terminal with the command: **sudo mysql;**

- Then, create a database named quiz with command: **create database quiz;**
- If the VM has root permissions, create a new user and grant the permissions using the following commands:

```sql
CREATE USER ‘jawadpasha’@‘localhost’ IDENTIFIED BY ‘Jawad@123’;
GRANT ALL PRIVILEGES ON quiz. * TO ‘jawadpasha’@‘localhost’;
```

- Go to the **/db** directory and type **mysql -p quiz < quiz.sql** to import the tables and records from the **.sql** file.

------------


### Step 2: Set up the project 

- After importing the project into the Eclipse IDE or any other IDE, update the **application.properties** file in all three modules services (admin, auth, quiz) inside the **src/main/resources/** package with the newly created user credentials or your VM MySQL credentials.

------------


### Step 3: Execute the project:

- Run all the 3 projects as Java Application.

- To explore the swagger, you can use the given url of the respective services and view the API swagger.

1. Auth Services: http://localhost:9200/swagger-ui/
2. Admin Services: http://localhost:9201/swagger-ui/
3. Quiz Services: http://localhost:9202/swagger-ui/

- To begin, you must use the login controller to generate the token that will allow you to test different controllers.

- The admin login credentails are:

	**Email:** admin@gmail.com and **Password:** 12345678

- In the Authorization field of any controller, the token has to be in the following format:

	`Bearer DKO1YyMykAC5wzNAt3kgx7jEsMuX/LRplAgNTXlbqwI=`

> **Note:** If you need full access, use the admin credentials for the login controller and replace the token with the above syntax.


