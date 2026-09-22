# Individual Assignment II: Oracle Pluggable Databases (PDB) Management

## 1. Overview of Tasks
This repository contains the technical documentation and evidence for Individual Assignment II in Database Development with PL/SQL (INSY 8311). The project covers the practical application of Oracle Multitenant Architecture, focusing on configuring Pluggable Databases (PDBs) and user privilege assignments.

## 2. Oracle Environment Used
* **Operating System:** Windows 11 (64-bit)
* **Database Edition:** Oracle Database 26ai
* **Tools Used:** SQL*Plus, Command Prompt (CMD), GitHub

## 3. Explanation of Each Task

### Task 1: Create a New Pluggable Database
A new pluggable database was successfully instantiated from the seed database template (`PDB$SEED`) using command-line administrative privileges in the root container (`CDB$ROOT`).
* **PDB Name:** `Bo_pdb_20252SEN266`
* **User Created:** `Bonnette_plsqlauca_20252SEN266`
* **Privileges Granted:** The local user account was assigned `CONNECT`, `RESOURCE`, and critical administrative session permissions to allow for persistent reuse across upcoming course laboratory modules.


### Task 2: Create and Delete a PDB
A separate temporary lifecycle database configuration was tested to demonstrate provisioning and complete system decommissioning workflows.
* **Temporary PDB Name:** `Bo_to_delete_pdb_20252SEN266`
* **Execution Workflow:** The database container was fully created, opened to verify availability, switched back to an intermediate closed status, and dropped permanently from the instance catalog along with its underlying operating system data files.

### Task 3: Oracle Enterprise Manager (OEM) Setup
* **Status:** Not Completed.
* **Reason:** Severe machine-specific port blockages and underlying service deployment errors prevented the local Oracle Express Management web interface from executing properly on the workstation. Extended remediation logs are documented in Section 4.

---

## 4. Challenges Faced & Solutions

### 1. Oracle Enterprise Manager (OEM) Port Binding & Timeout Failures
* **Problem:** During the execution of Task 3, running configuration verification calls like `dbms_xdb_config.gethttpsport` failed to securely bind or expose the management UI. Attempting to connect via the browser console yielded indefinite server connection timeouts and SSL layer protocol validation drops.

* **Troubleshooting Steps Taken:** Checked local operational logs using `lsnrctl status` to guarantee that the primary database listener was intercepting system requests. Local Windows firewall exceptions were briefly added for ports `5500` and `5501` along with localized router loopback checks. The database engine configuration files resisted binding to a accessible network interface layout on this specific operating system setup.

* **Resolution:** To preserve assignment delivery timelines, standard administrative SQL terminal access via SQL*Plus was used as an absolute replacement to execute and fulfill the database architectures required in Tasks 1 and 2.

---

## 5. Academic Integrity Statement
"I declare that this submission is entirely my own individual work. I have performed all configuration tasks independently. I have not copied any commands, solutions, or screenshots from my classmates, nor have I utilized prohibited AI generation tools for my database commands."

---

## 6. Required Submission Details Block
* **Repository Link:** https://github.com/Bonnette26/Oracle_pdb_ass_II_20252SEN266_Bonnette
* **PDB Name Created:** Bo_pdb_20252SEN266
* **Issues Encountered:** Yes
