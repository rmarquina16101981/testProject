ITK RESERVATION API
===================

1. Introduction
-------------------------
    
This API project will obtain information from different vendors (MindBody, JackRabbit, etc), such as:

* Activities (class)
* Clients
* Providers (barron gymastics, etc.)
* Location
* Instructors

This project contains the next packages
* ITKReservationEJB
* ITKReservationWEB
* IKTReservationEAR
* ITKReservationAPI


2. Requirements
-------------------------
You should have installed:
* *GlassFish 3 [download](http://glassfish.java.net/public/downloadsindex.html).*
* *Mysql 5 [download](http://dev.mysql.com/downloads/).* 
* *Maven 2 [download](http://maven.apache.org/download.cgi).* 


3. Deploy reservation API on Glassfish
-------------------------
* Step 1 : download or clone "ITK_Reservation_api" project.
* Step 2 : Run the database sql script in the mysql folder (~/mysql/reservation.sql), the database reservation will be created, this name will be referenced in next steps.
* Step 3 : Ensure all applications (EAR, EJB, and WEB) use Glassfish server.
* Step 4 : At Glassfish configurations (at localhost:4848), add a "JDBC Conections Pool" (under Resources/JDBC) with parameters: 
    * Pool name: mysql_reservation_rootPool 
    * Resource type: javax.sql.DataSource 
    * Database Driver Vendor : com.mysql.jdbc.jdbc2.optional.MysqlDataSource
* Step 5 : At Glassfish configurations, add a "JDBC Resource" (under Resources/JDBC) with parameters: 
    * JNDI Name: jdbc/reservation
    * Pool Name: mysql_reservation_rootPool
* Step 6 : Build the project with command line `mvn -X package > mvn.log` 
* Step 7 : Deploy the reservation.ear (~/ITKReservationAPI/Target/) in glassfish


4. Copyrigth
-------------------------
   @ItivityKids Inc.

   *Web page: [www.itivitykids.com](http://www.itivitykids.com).*

