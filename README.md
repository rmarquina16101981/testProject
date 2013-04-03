ITK RESERVATION API
===================

1. Introduction
-------------------------
    
This API project will obtain information from diferent vendors (mindbody, jackrabbit, etc), such as:

* Activities (class)
* Clients
* Providers (barron gymastics, etc.)
* Location
* Instructors

This project contain  the next packages
* ITKReservationEJB
* ITKReservationWEB
* IKTReservationEAR
* ITKReservationAPI


2. Requirements
-------------------------
You should have installed and configured:
* *GlassFish 3 [dowload](http://glassfish.java.net/public/downloadsindex.html).*
* *Mysql 5 [dowload](http://dev.mysql.com/downloads/).* 
* *Maven 2 [dowload](http://maven.apache.org/download.cgi).* 


3. How to use
-------------------------
* Step 1 : download or clone "ITK_Reservation_api" project.
* Step 2 : Run the database sql script in the mysql folder (~/mysql/reservation.sql), the dabase reservation will be created, this name will be referenced in next steps.
* Step 3 : Ensure all applications (EAR, EJB, and WEB) use Glassfish server.
* Step 4 : At Glassfish configurations (at localhost:4848), add a "JDBC Conections Pool" (under Resources/JDBC) with parameters: 
    * Pool name: mysql_reservation_rootPool 
    * Resource type: javax.sql.DataSource 
    * Database Driver Vendor : com.mysql.jdbc.jdbc2.optional.MysqlDataSource
* Step 5 : At Glassfish configurations, add a "JDBC Resource" (under Resources/JDBC) with parameters: 
    * JNDI Name: jdbc/reservation
    * Pool Name: mysql_reservation_rootPool
* Step 6 : Build the project with command line `mvn package` 
* Step 7 : Deploy the reservation.ear (~/ITKReservationAPI/Target/) in glassfish


4. Copyrigth
-------------------------
   @ItivitiKids Inc.

   *Web page: [www.itivitikids.com](http://www.itivitikids.com).*

