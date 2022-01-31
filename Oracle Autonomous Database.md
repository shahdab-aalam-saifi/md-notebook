# Oracle Autonomous Database

> ##### https://techgoeasy.com/1z0-931-questions-and-answers/

1. Which open source orchestration tool can be used to provision autonomous database resources in Oracle Cloud Infrastructure?
   1. Enterprise Manager
   2. Dlocker
   3. **Terraform**
   4. REST API
2. Which statement is false about Autonomous Database Oracle Client Credentials (Wallets)?
   1. **The Wallet for the Autonomous Database is the same as the Transparent Data Encryption (TDE) wallet**
   2. The Oracle Client Credential file is downloaded as a ZIP file.
   3. In addition to the Oracle Client Credential Wallet, a user must have a username and password in order to connect to the Autonomous Database.
   4. You MUST have an Oracle Client Credential Wallet in order to connect to the Autonomous Database
3. What is the default retention period for both Automatic and Manual Autonomous Database Backups?
   1. **60 days**
   2. 30 days
   3. One Year
   4. 7 days
4. Which is NOT required to connect to Autonomous Database from SQL developer?
   1. Username and password
   2. **Database name**
   3. Wallet file
   4. Service name
5. Which two statements are true about the Oracle Cloud Infrastructure (OCI)? (Choose two.)
   1. A single fault domain can be associated with multiple regions and availability domains
   2. **Because availability domains do not share infrastructure such as power or cooling, or the internal availability domain network, a failure at one availability domain within a region is unlikely to impact the availability of the others within the same region.**
   3. **An OCI region is a localized geographic area, and an availability domain is one or more data centers located within a region.**
   4. Regions are dependent on other regions and must be located with 5 thousand kilometers of each other.
6. Which three statements are true regarding how Autonomous Database provides data security? (Choose three.)
   1. **Oracle automatically applies security updates to ensure data is not vulnerable to known attack vectors.**
   2. **Network connections from clients to Autonomous Database are encrypted using the client credentials wallet.**
   3. Users are given OS logons or SYSDBA privileges to prevent phishing attacking.
   4. **Data is encrypted at rest using transparent data encryption.**
7. What are two advantages of using Data Pump to migrate your Oracle Databases to Autonomous Database? (Choose two.)
   1. Data Pump is faster to migrate database than using RMAN
   2. **Data Pump is platform independent - it can migrate Oracle Databases running on any platform.**
   3. Data Pump creates the tablespaces used by your Autonomous Database
   4. **Data Pump can exclude migration of objects like indexes and materialized views that are not needed by Autonomous Database**
8. What predefined user is created when an Autonomous Database (ADB) instance is created that you connect to in order to create other users and grant roles?
   1. SYS
   2. **ADMIN**
   3. SCOTT
   4. DWDEV
9. Which two statements are true with regards to Oracle Data Sync? (Choose two.)
   1. **Data Sync can connect to any jdbc compatible source like MongoDB, RedShift and Sybase.**
   2. Data Sync can use a normal OCI (thick) client connection to connect to an Oracle database.
   3. Data Sync can load your data in parallel in order to speed up the loading process.
   4. **Data Sync has default drivers available that supported loading data fromDB2, Microsoft SQL Server, MySQL and Teradata.**
10. Which of these database features is NOT part of the Autonomous Database?
    1. Real Application Clusters (RAC)
    2. Flashback Database
    3. Online Indexing
    4. **Java in the Database**

11. Which task is NOT automatically performed by the Oracle Autonomous Database?
    1. Backing up the database.
    2. **Mask your sensitive data.**
    3. Automatically optimize the workload.
    4. Patching the database.

12. Which Autonomous Database Cloud service ignores hints in SQL Statements by default?
    1. Both services ignore hints by default.
    2. Neither service ignores hints by default.
    3. Autonomous Transaction Processing
    4. **Autonomous Data Warehouse**

13. How many pre-defined service names are configured in tnsnames.ora for a single Autonomous Transaction Processing database instance, and what are they called?
    1. **Five. They are called tpurgent, tp, high, medium and low**
    2. None. There are no pre-defined service names in tnsnames.ora
    3. Three. They are called high, medium and low
    4. Two. They are called ATP and ADW

14. What are the two methods that could be used during the migration of your existing Oracle database to Autonomous Database?(Choose two.)
    1. **Data Pump**
    2. CSV files copied to Autonomous Database block storage
    3. **Golden Gate**
    4. Recovery Manager (RMAN)

15. What predefined user is created when an Autonomous Database (ADB) instance is created that you connect to in order to create other users and grant roles?
    1. SYS
    2. SCOTT
    3. DWDEV
    4. **ADMIN**

16. The default eight-day retention period for Autonomous Database performance data can be modified using which DBMS_WORKLOAD_REPOSITORY subprogram procedure
    1. CREATE_BASELINE_TEMPLATE
    2. **MODIFY_SNAPSHOT_SETTINGScorrect**
    3. MODIFY_BASELINE_WINDOW_SIZE
    4. UPDATE_OBJECT_INFO

17. Which is the correct subset of services offered via OCI-CLI (command line interface) for Autonomous Database via calls made to the OCI API's?
    1. **Create, Get, List, Stop, Restore**
    2. Create, Query, Update, List, Start
    3. Start, Delete, Update, Query, Stop
    4. Create, Query, List, Stop, Restore

18. Which operating system can Data Visualization Desktop be run on?
    1. Solaris
    2. **Windows**
    3. Linux
    4. AIX

19. When exporting a notebook, what type of file is created?
    1. **JSON**
    2. TXT
    3. D. SQL
    4. XML

20. Which can be Scaled independently of the number of CPUs in an Autonomous Database
    1. **Storage**
    2. Concurrency
    3. Memory
    4. Parallelism
    5. Sessions

21. Where can a user's public ssh key be added on the Oracle Cloud Infrastructure Console in order to execute API calls?
    1. SSH keys are not required in Oracle Cloud Infrastructure
    2. **Navigate to Identity, select Users panel on the console and select "Add Public Key".correct**
    3. On the Autonomous Database Console.
    4. SSH keys cannot be added from console. They have to be added using REST APIs only.

22. Users are required to select a service when connecting to Autonomous Data Warehouse and these services match to one of three different consumer groups: High, Medium, and Low.
    Which statement about these consumer groups is correct?
    1. High provides highest resources, lowest concurrency, and DoP is 1.
    2. High provides highest concurrency and lowest resources, and DoP is i.
    3. **Low provides highest concurrency, lowest resources, and DoP = 1.**
    4. Medium provides intermediate resource and concurrency, and queries run in a serial.

23. Which is the default port use ADB after creation
    1. 1551
    2. 1521
    3. 1561
    4. **1522**

24. Which two options are available to restore an Autonomous Data Warehouse? (Choose two.)
    1. Select the archived redo logs.
    2. Select the snapshot of the backup.
    3. **Select the backup from which restore needs to be done.**
    4. Backup and recovery must be done using Recovery Manager(RMAN).
    5. **Specify the point in time (timestamp) to restore**





