# Assignment8
# Executive Summary
This week we will be going over what Database Administratory Responsibilities and what they do, The five log files and what they mean, status and server variables and the four levels of privileges and how to grant them. 
# Database Administrator Responsibilities
The main responsibilities of a Database Administrator are: Maintenance, Design, Security, and Backup. Maintenance for a DBA include monitoring the server, configuring the server, and maintaining log files. Design is the action of designing and creating the database. Security maintains the user accounts and secures the server and its databases. Backup is backing up the database regularly, restoring the database if needed, and moving all of the database information to another database if needed. 
# Log Files
There are five log files that are discussed in our book. The log files are: General, Error, Slow Query, Binary, and Relay. General log files are a text file that contain a record of client connections. Error log files are a text file that contains messages of startup, shutdown, and error messages for a server. Slow Query log files are a text file that contains SQL statement that take a long time to execute. Binary log files are one or more binary files that contain the record of changes made to a database. Last, Relay log files that are one or more binary files that are used on a slave machine to relay any changes that have been made on the master machine. 
# Variables
The status variables are to conatain information on the status of the MySQL server. An example of status variables would be Bytes_sent which is the number of bytes sent to all clients. 
The server variables are to store a setting for the current configuration of the MySQL server. An example of system variables would be admin_address which is the IP address needed to listen for connections on the administrative network interface.
# Privileges
A. Explain the following code (copy and paste the code into your readme.md file and comment all sections):
This code is creating guitar_admin@localhost. The the grant all is giving this newly created user global privileges. The second grant is giving the newly created user just database privileges.    

CREATE USER guitar_admin@localhost IDENTIFIED BY 'pa55word'; 
CREATE USER guitar_admin@localhost IDENTIFIED BY 'pa55word';  CREATE USER guitar_user@localhost IDENTIFIED BY 'pa55word'; 
  
GRANT ALL 
ON guitar.* 
TO guitar_admin@localhost; 
  
GRANT SELECT, INSERT, UPDATE, DELETE  ON guitar.* 
TO guitar_user@localhost; 
 
B. What are the privilege levels that can be granted to a user? 
Global, Database, Table, and Column privileges are the four privilege levels that can be granted to a user 
 
C. How would this code change to grant column privileges to the customer first_name, last_name and email_address? 
To grant column privileges to this user the grant statement should look like this
GRANT SELECT (first_name, last_name, email_address), UPDATE (customers) ON guitar.* TO guitar_user@localhost;

 
D. Why would you want to do this? 
Being able to give specific people different privileges in SQL would be beneficial because you could give entry level developers less taxing work compared to senior level developers.
# Conclusion
To wrap up the end of this semester, we learned database administration responsibilities, log files, status and server variables, and what the four levels of privileges are. 
