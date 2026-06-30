# oracle_pdb_assignment2_31383_2025_valentin
## 1. Assignment Overview
This assignment demonstrates practical Oracle Multitenant Architecture skills,
including creating and managing Pluggable Databases (PDBs), configuring users,
and accessing Oracle Enterprise Manager.

## 2. Oracle Environment
- **Oracle Version:** Oracle Database 21c (or your version)
- **Operating System:** Windows 10 / Oracle Linux (your OS)
- **Tools Used:** SQL*Plus, Oracle Enterprise Manager Express, GitHub

## 3. Task Documentation

### Task 1 — PDB Creation & User Setup
- Created PDB: `er_pdb_2024101`
- Opened the PDB and verified its status
- Created user: `eric_plsqlauca_2024101`
- Granted CONNECT, RESOURCE, DBA, and CREATE SESSION privileges
- Successfully connected using the new user

### Task 2 — Temporary PDB Creation & Deletion
- Created temporary PDB: `er_to_delete_pdb_2024101`
- Verified it existed using v$pdbs
- Opened and then dropped it using `DROP PLUGGABLE DATABASE ... INCLUDING DATAFILES`
- Confirmed deletion by re-querying v$pdbs

### Task 3 — OEM Configuration
- Accessed Oracle Enterprise Manager at https://localhost:5500/em
- Verified the created PDB appears in the OEM dashboard
- Captured screenshots of database instance and PDB information

## 4. Challenges and Solutions
- **Challenge:** File path errors during PDB creation
  **Solution:** Verified the correct ORADATA path using `v$datafile`
- **Challenge:** OEM port not responding
  **Solution:** Reconfigured HTTPS port using `DBMS_XDB_CONFIG.SETHTTPSPORT(5500)`

## 5. Lessons Learned
- Understood the CDB/PDB Multitenant architecture model
- Learned how to create, open, close, and drop PDBs
- Practiced user creation and privilege management inside PDBs
- Gained experience with Oracle Enterprise Manager

## 6. Integrity Statement
I confirm that this assignment represents my own practical work, screenshots, 
and documentation. All external resources consulted have been properly acknowledged.
