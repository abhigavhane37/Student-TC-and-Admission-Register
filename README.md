# Student-TC-and-Admission-Register

**STAR** is a Python-based project designed to manage student admission and transfer certificate (TC) records efficiently.
The project leverages MySQL for data storage and provides functionalities to insert, update, delete, and search records. 

## Objectives

The primary objectives of the **STAR** project are:
1. Computerize admission records.
2. Computerize Transfer Certificate (TC) records.
3. Enable updating of admission records.
4. Allow searching of single and multiple records.

## Platform and Technologies
- **Operating System**: Windows XP or higher  
- **Programming Language**: Python  
- **Data Storage**: MySQL  

## Table Structures
### Table: `Admn`

| **Sr. No.** | **Field Name**  | **Datatype** | **Size** | **Remark**      |
|-------------|-----------------|--------------|----------|-----------------|
| 1           | `Admn_no`       | `Int`        | 6        | Primary Key     |
| 2           | `Dateofadmn`    | `Varchar`    | 10       |                 |
| 3           | `Name`          | `Char`       | 30       |                 |
| 4           | `Father_name`   | `Char`       | 30       |                 |
| 5           | `Mother_name`   | `Char`       | 30       |                 |
| 6           | `DOB`           | `Varchar`    | 10       |                 |
| 7           | `Admn_Cat`      | `Varchar`    | 3        |                 |
| 8           | `Class`         | `Varchar`    | 4        |                 |
| 9           | `Caste`         | `Char`       | 10       |                 |
| 10          | `TC_no`         | `Int`        | 10       |                 |
| 11          | `TC_date`       | `Varchar`    | 10       |                 |

### Table: `TC`

| **Sr. No.** | **Field Name** | **Datatype** | **Size** | **Remark**      |
|-------------|----------------|--------------|----------|-----------------|
| 1           | `TC_no`        | `Int`        | 10       | Primary Key     |
| 2           | `TC_date`      | `Varchar`    | 10       |                 |
| 3           | `Admn_no`      | `Int`        | 6        | Foreign Key     |
| 4           | `Name`         | `Char`       | 30       |                 |
| 5           | `Reason`       | `Char`       | 30       |                 |
| 6           | `Remark`       | `Char`       | 100      |                 |

## Functionalities

### Operations on `Admn` Table:
1. Insert Student Details.  
2. Update Student Details.  
3. Delete Student Details.  
4. Search Individual Student Details.  
5. Search All Student Details.  
6. Exit.

### Operations on `TC` Table:
1. Insert TC Details.  
2. Update TC Details.  
3. Delete TC Details.  
4. Search Individual TC Details.  
5. Search All TC Details.  
6. Exit.

## How to Run the Project

1. Clone the repository:
   bash
   git clone https://github.com/your-username/STAR-Student-TC-and-Admission-Register.git
   
2. Install required Python dependencies:
   bash
   pip install mysql-connector-python
   
3. Create the database in MySQL and tables using the structure provided above.

4. Update the `connect_to_db` function with your database credentials:
   python
   conn = mysql.connector.connect(
       host='localhost',
       user='your_username',
       password='your_password',
       database='STAR'
   )
   
5. Run the main script:
   bash
   python main.py
   



