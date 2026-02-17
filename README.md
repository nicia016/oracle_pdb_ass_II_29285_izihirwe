# oracle_pdb_ass_II_29285_izihirwe
# Oracle Pluggable Database Assignment II

Repository Name: oracle_pdb_ass_II_29285_izihirwe  
Course: Advanced Database Systems  
Student Name: Izihirwe  
Student ID: 29285  
Year: 2026  

---

## Overview

This assignment states practical implementation of Oracle Multitenant Architecture using Pluggable Databases (PDBs).

The following tasks were completed:

1. Creation of a new Pluggable Database (PDB)
2. Creation of a user inside the PDB
3. Creation and complete deletion of a temporary PDB
4. Configuration and access of Oracle Enterprise Manager (OEM)
5. Documentation and evidence submission

---

## Oracle Environment Used

- Oracle Version: Oracle Database 19c  
- Architecture: Multitenant (CDB + PDB)  
- Operating System: Windows  
- SQL Tool Used: SQL*Plus  
- OEM URL: https://localhost:5500/em  

---

# Task 1 – Create a New Pluggable Database

## PDB Naming Convention Used

PDB Name:

```
iz_pdb_29285
```

## User Created Inside PDB

Username:

```
izihirwe_plsqlauca_29285
```

Password:  
(Simple password chosen and remembered securely)

---

## Steps Performed

1. Connected to CDB as SYSDBA
2. Executed CREATE PLUGGABLE DATABASE command
3. Opened the PDB using:
   ```
   ALTER PLUGGABLE DATABASE iz_pdb_29285 OPEN;
   ```
4. Verified open state using:
   ```
   SHOW PDBS;
   ```
5. Changed session to the PDB:
   ```
   ALTER SESSION SET CONTAINER=iz_pdb_29285;
   ```
6. Created user:
   ```
   CREATE USER izihirwe_plsqlauca_29285 IDENTIFIED BY password;
   ```
7. Granted privileges:
   ```
   GRANT CONNECT, RESOURCE TO izihirwe_plsqlauca_29285;
   ```

---

## Verification

- PDB created successfully
- PDB open mode verified
- User successfully created inside the PDB
- Username clearly visible in SQL output screenshots

📷 Screenshots available in:
```
![Image Alt](https://github.com/nicia016/oracle_pdb_ass_II_29285_izihirwe/blob/d89fe84c453ad8f0686df0a9a6cdc810ca4a194c/sqlpl%202/ceate%20-pdb.png)
```

---

# Task 2 – Create and Delete a Temporary PDB

## Temporary PDB Naming Convention

PDB Name:

```
iz_to_delete_pdb_29285
```

---

## Steps Performed

1. Created temporary PDB
2. Verified using:
   ```
   SHOW PDBS;
   ```
3. Closed PDB:
   ```
   ALTER PLUGGABLE DATABASE iz_to_delete_pdb_29285 CLOSE IMMEDIATE;
   ```
4. Dropped PDB including datafiles:
   ```
   DROP PLUGGABLE DATABASE iz_to_delete_pdb_29285 INCLUDING DATAFILES;
   ```
5. Verified deletion using:
   ```
   SHOW PDBS;
   ```

---

## Verification

- Temporary PDB successfully created
- PDB successfully deleted
- Confirmed it no longer exists in CDB

📷 Screenshots available in:
```
screenshots/pdb_deletion/
```

---

# Task 3 – Oracle Enterprise Manager (OEM)

Oracle Enterprise Manager was configured and accessed successfully.

OEM Dashboard confirmed:

- Oracle Database environment running
- Created PDB (iz_pdb_29285)
- Active services
- Username izihirwe_plsqlauca_29285 visible

OEM URL:
```
https://localhost:5500/em
```

📷 Screenshot available in:
```
screenshots/oem_dashboard/
```

---

# Challenges Faced

- Ensuring correct container before creating user
- Opening PDB after creation
- Verifying listener and OEM service

All issues were resolved using proper SQL commands and environment verification.

---

# Conclusion

This assignment successfully demonstrated:

- Oracle Multitenant Architecture usage
- PDB creation and management
- User creation inside PDB
- Safe deletion of a PDB
- Oracle Enterprise Manager monitoring

The environment is fully configured and ready for future coursework.

---

# Integrity Statement

I confirm that this work is my own implementation.  
All commands were executed personally in my Oracle environment.  
No unauthorized assistance was used in completing this assignment.

Signed,  
Izihirwe  
29285
