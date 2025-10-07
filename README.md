# IrembereOlivier_plsqlauca_28392
AUCA PL/SQL Assignment This project demonstrates how to create, open, delete, and manage Pluggable Databases (PDBs) in Oracle 23c Free. It also includes configuration of Oracle Enterprise Manager (EM Express) for database monitoring and administration.


# Oracle Database Administration Project — AUCA PL/SQL Assignment

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

## Task 1: Create a New Pluggable Database (PDB)

### ✅ SQL Command Used
```sql
CREATE PLUGGABLE DATABASE PLSQL_AUCA_28392DB 
ADMIN USER IREMBERE IDENTIFIED BY kwiga 
FILE_NAME_CONVERT = (
  'C:\app\USER\oradata\FREE\pdbseed',
  'C:\App\oradata\oradata\FREE\PLSQL_AUCA_28392DB'
);
