1 Project structure:                                                                                              
    • php-mysql-docker/                                                                                            
       • index.php                                                                                                 
       • Dockerfile                                                                                                
       • docker-compose.yml                                                                                        
       • init.sql                                                                                                  
2 To run the application:
  a. Open a terminal and navigate to the 'php-mysql-docker' directory.
  b. Run the following command to build and start the containers:                                                            
     docker-compose up -d --build                                                                                   
  c. Wait for the containers to start up. This may take a few moments.                                            
3 To test the application: a. Open a web browser and go to http://localhost:8080 b. You should see a message      
   "Connected successfully to MySQL database!" followed by a list of users from the database.                      

4 To stop the application:
  a. In the terminal, run:                                                               
    docker-compose down                                                                                            
                                                                                                                   
                                                                                                                   
Here's an explanation of what each file does:                                                                      
                                                                                                                   
 1 index.php: This is our main PHP application file. It connects to the MySQL database, runs a query to fetch all  
   users, and displays the results.                                                                                
 2 Dockerfile: This file defines how to build the PHP Docker image. It uses the official PHP 7.4 Apache image,     
   installs the mysqli extension, and copies our application files into the container.                             
 3 docker-compose.yml: This file defines our multi-container Docker application. It sets up two services:          
    • 'web': Our PHP application, built from the Dockerfile.                                                       
    • 'db': A MySQL 5.7 database. It also sets up volumes for data persistence and networking between the          
      containers.                                                                                                  
 4 init.sql: This SQL script creates the 'users' table and inserts some initial data. It's automatically executed  
   when the MySQL container starts for the first time.                                                             
                                                                                                                   
This setup demonstrates a basic dockerized PHP application with a MySQL database. It's a good starting point for   
learning about Docker and Docker Compose with PHP and MySQL.                                                       
