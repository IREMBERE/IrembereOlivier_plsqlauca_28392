
# DATABASE CREATION ,DELETION AND OEM PROJECT — AUCA PL/SQL Assignment

This project demonstrates how to create, open, delete, and manage Pluggable Databases (PDBs) in Oracle 23c Free. It also includes configuration of Oracle Enterprise Manager (EM Express) for database monitoring and administration.


## 👨‍💻 Student Information
- **Name:** IREMBERE Olivier  
- **Student ID:** 28392  
- **Course:** PL/SQL Programming  
- **Institution:** Adventist University of Central Africa (AUCA)  
- **Database Version:** Oracle Database 23c Free  
- **Tool Used:** SQL*Plus & Oracle EM Express (port 5500)

---

## Project Objective
This project demonstrates how to **create, manage, and delete Pluggable Databases (PDBs)** using Oracle 23c Free, and how to **configure Oracle Enterprise Manager Express (EM Express)** for monitoring and administration.

---

## TASK 1: CREATE A NEW PLUGGABLE DATABASE 
In this task, we created a new Pluggable Database (PDB) inside the Oracle Container Database (CDB).
The goal was to understand how to define an admin user, assign roles, and use the FILE_NAME_CONVERT clause to specify the new PDB’s datafile location.

### This is  the SQL Command i Used
sql

CREATE PLUGGABLE DATABASE plsql_class2025db 
ADMIN USER olivier_plsqlauca_28392 IDENTIFIED BY Oracle123 
ROLES = (DBA)
DEFAULT TABLESPACE users 
DATAFILE 'C:\app\USER\oradata\ORCL\plsql_class2025db\users01.dbf' 
SIZE 250M AUTOEXTEND ON 
FILE_NAME_CONVERT = (
  'C:\app\USER\oradata\ORCL\pdbseed\', 
  'C:\app\USER\oradata\ORCL\plsql_class2025db\'
);

![Pluggable DB](https://githubusercontent.com/IREMBERE/IrembereOlivier_plsqlauca_28392/blob/main/creatig%20pluggable%20database.png?raw=true)

## TASK 2 CREATE AND DELETE A PDB 

This task focused on creating another PDB and then deleting it.
It helped demonstrate how to manage PDB lifecycles — from creation using the CREATE PLUGGABLE DATABASE statement to safely removing it with the DROP PLUGGABLE DATABASE command.

### This is the SQL Cmmand line i used 

sql

CREATE PLUGGABLE DATABASE ol_to_delete_pdb_28392 
ADMIN USER olivier_plsqlauca_28392 IDENTIFIED BY Oracle123 
ROLES = (DBA) 
DEFAULT TABLESPACE users 
DATAFILE 'C:\app\USER\oradata\ORCL\ol_to_delete_pdb_28392\users01.dbf' SIZE 250M AUTOEXTEND ON 
FILE_NAME_CONVERT = ('C:\app\USER\oradata\ORCL\pdbseed\', 'C:\app\USER\oradata\ORCL\ol_to_delete_pdb_28392\');

## Step 2 Delete the PDB

### this is the SQL command line i used 
sql

DROP PLUGGABLE DATABASE ol_to_delete_pdb_28392 INCLUDING DATAFILES;

## TASK 3 ORACLE ENTERPRISE MANAGER
In this task, we configured Oracle Enterprise Manager to monitor and manage our database environment.
The goal was to access the OEM dashboard through a web interface and verify that all created databases were running successfully.



## NOTES AND REFLECTIONS

This task helped me understand how to manage pluggable databases in Oracle.
At first, I faced issues while connecting and setting the correct paths for the datafiles.
After consulting YouTube tutorials and class notes, I learned the correct directory structure and syntax, which helped me successfully create and drop the PDB.

It was challenging because it was my first time using Oracle Database, but it was also a valuable learning experience.





