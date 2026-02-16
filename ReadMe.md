# Oracle Pluggable Database Management – Assignment II

Kamanzi Thierry  
Student ID: 27215  
Database Development with PL/SQL (INSY 8311)  

---

## Overview

This assignment demonstrates practical understanding of Oracle Multitenant Architecture and Pluggable Database (PDB) management. The work involved creating and managing Pluggable Databases, creating users inside a PDB, deleting a temporary PDB, accessing Oracle Enterprise Manager (OEM), and documenting all activities professionally on GitHub.

The Oracle environment used for this assignment was Oracle Database 21c, SQL*Plus, and Oracle Enterprise Manager (OEM) running on Windows 11.

---

## Main Pluggable Database Creation

The required main Pluggable Database was created using the exact naming convention:

th_pdb_27215

After connecting as SYSDBA and ensuring the session was set to CDB$ROOT, the PDB was successfully created and opened. The status was verified using the V$PDBS view.

Inside the newly created PDB, the required user was created with the exact naming convention:

thierry_plsqlauca_27215

The user was granted CONNECT and RESOURCE privileges. Verification was performed using DBA_USERS to confirm that the account exists and is properly configured.

The creation process was successful and is supported by screenshots included in this repository.

---

## Temporary PDB Creation and Deletion

A temporary PDB was created using the required naming format:

th_to_delete_pdb_27215

The PDB was successfully created and opened. Its existence was verified using V$PDBS.

After verification, the temporary PDB was properly closed and completely removed using:

DROP PLUGGABLE DATABASE INCLUDING DATAFILES;

A final check confirmed that the temporary PDB no longer exists in the system.

This demonstrates correct understanding of PDB lifecycle management.

---

## Oracle Enterprise Manager (OEM) Verification

Oracle Enterprise Manager was accessed through:

https://localhost:5500/em

The system was accessed using SYS as SYSDBA credentials. From the OEM dashboard, the Oracle environment was visible, including:

- The main PDB (th_pdb_27215)
- The created user (thierry_plsqlauca_27215)
- The container database environment

The dashboard confirms successful execution of the required administrative tasks. A clear screenshot of the OEM dashboard is included in this repository.

---

## Screenshots

All evidence screenshots are stored inside the `screenshots/` folder. These include:

- PDB creation
  https://github.com/Thierry710/oracle_pdb_ass_II_27215_thierry/blob/1aee4f25238692468df4497e41b1db3dab0c0c5c/Screenshots/pdb_creation/db%201.1.png
- PDB open state
- https://github.com/Thierry710/oracle_pdb_ass_II_27215_thierry/blob/1aee4f25238692468df4497e41b1db3dab0c0c5c/Screenshots/pdb_creation/db%201%20.png
- User creation
- https://github.com/Thierry710/oracle_pdb_ass_II_27215_thierry/blob/1aee4f25238692468df4497e41b1db3dab0c0c5c/Screenshots/pdb_creation/db%202.1.png
- Temporary PDB creation
- https://github.com/Thierry710/oracle_pdb_ass_II_27215_thierry/blob/1aee4f25238692468df4497e41b1db3dab0c0c5c/Screenshots/pdb_deletion/db%203.1.png
- Temporary PDB deletion
- https://github.com/Thierry710/oracle_pdb_ass_II_27215_thierry/blob/1aee4f25238692468df4497e41b1db3dab0c0c5c/Screenshots/pdb_deletion/db%203.1.png
- OEM dashboard verification
-https://github.com/Thierry710/oracle_pdb_ass_II_27215_thierry/blob/1aee4f25238692468df4497e41b1db3dab0c0c5c/Screenshots/oem_dashboard/db%20dashboard%20.png
-https://github.com/Thierry710/oracle_pdb_ass_II_27215_thierry/blob/1aee4f25238692468df4497e41b1db3dab0c0c5c/Screenshots/oem_dashboard/db%20dashboard%202.png
Each screenshot clearly displays commands and results as required.

---

## Challenges Encountered

During the process, an ORA-01031 (insufficient privileges) error occurred when attempting to open the PDB. This issue was resolved by reconnecting as SYSDBA and ensuring the session was set to CDB$ROOT before executing administrative commands.

After correcting the privilege level, all operations were executed successfully without further issues.

---

## Repository Information

Repository Name:  
oracle_pdb_ass_II_27215_thierry  

Visibility: PUBLIC  

---

## Submission Details

Repository Link: https://github.com/Thierry710/oracle_pdb_ass_II_27215_thierry.git  
PDB Name Created: th_pdb_27215  
Issues Encountered: Yes (ORA-01031 – resolved successfully)

---

## Integrity Statement

I confirm that this assignment was completed individually. All commands were executed and verified personally in my Oracle environment in accordance with academic integrity standards.

---

## Conclusion

This assignment strengthened my practical understanding of Oracle Multitenant Architecture, Pluggable Database management, user administration within a PDB, and Oracle Enterprise Manager monitoring. The experience gained prepares me for future PL/SQL laboratories, practical assessments, and database administration tasks.
