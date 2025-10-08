# BANCO-DE-DADOS-

**DATABASE**

A database is an organized collection of structured information or data, typically stored electronically in a computer system. A database is usually controlled by a Database Management System (DBMS). Together, the data and the DBMS, along with the associated applications, are called a database system, often shortened to just database.

Data can be easily accessed, managed, modified, updated, controlled, and organized. Most databases use Structured Query Language (SQL) for writing and querying data.

## SQL

SQL is a programming language used by almost all relational databases to query, manipulate, and define data, and to provide access control. SQL was first developed at IBM in the 1970s, with Oracle being a major contributor, which led to the implementation of the ANSI SQL standard. SQL has spurred many extensions from companies like IBM, Oracle, and Microsoft.

## DATA TYPES IN MYSQL

MySQL is the world's best-known open-source database management system. Databases are the essential data repositories for all software applications. For example, whenever someone performs a web search, logs into an account, or completes a transaction, a database stores the information so it can be accessed in the future.

### Data Types Used

#### String

SQL String Functions are built-in functions that allow us to manipulate and process text data stored in a database. Common examples of text fields include names, descriptions, and addresses.

| Data Type | Description |
|-----------|-------------|
| CHAR(size) | A FIXED length string (can contain letters, numbers, and special characters). The _size_ parameter specifies the column length in characters - can be from 0 to 255. Default is 1 |
| VARCHAR(size) | A VARIABLE length string (can contain letters, numbers, and special characters). The _size_ parameter specifies the maximum string length in characters - can be from 0 to 65535 |
| BINARY(size) | Equal to CHAR(), but stores binary byte strings. The _size_ parameter specifies the column length in bytes. Default is 1 |
| VARBINARY(size) | Equal to VARCHAR(), but stores binary byte strings. The _size_ parameter specifies the maximum column length in bytes. |
| TINYBLOB | For BLOBs (Binary Large Objects). Max length: 255 bytes |
| TINYTEXT | Holds a string with a maximum length of 255 characters |
| TEXT(size) | Holds a string with a maximum length of 65,535 bytes |
| BLOB(size) | For BLOBs (Binary Large Objects). Holds up to 65,535 bytes of data |
| MEDIUMTEXT | Holds a string with a maximum length of 16,777,215 characters |
| MEDIUMBLOB | For BLOBs (Binary Large Objects). Holds up to 16,777,215 bytes of data |
| LONGTEXT | Holds a string with a maximum length of 4,294,967,295 characters |
| LONGBLOB | For BLOBs (Binary Large Objects). Holds up to 4,294,967,295 bytes of data |
| ENUM(val1, val2...) | A string object that can have only one value, chosen from a list of possible values. You can list up to 65535 values in an ENUM list. If a value is inserted that is not in the list, a blank value will be inserted. The values are sorted in the order you enter them |
| SET(val1, val2...) | A string object that can have 0 or more values, chosen from a list of possible values. You can list up to 64 values in a SET list |

#### Numeric

The exact numeric data types in SQL consist of the NUMERIC(p,s) and DECIMAL(p,s) subtypes. They are exact, defined by precision (p) and scale (s). Precision is an integer representing the total number of digits allowed in this column. Scale represents the number of decimal places to the right (if positive) or left (if negative) of the decimal point.

| Data Type | Description |
|-----------|-------------|
| BIT(size) | A bit-value type. The number of bits per value is specified in _size_. The _size_ parameter can hold a value from 1 to 64. The default value for _size_ is 1. |
| TINYINT(size) | A very small integer. Signed range is from -128 to 127. Unsigned range is from 0 to 255. The _size_ parameter specifies the maximum display width (which is 255) |
| BOOL | Zero is considered as false, nonzero values are considered as true. |
| BOOLEAN | Equal to BOOL |
| SMALLINT(size) | A small integer. Signed range is from -32768 to 32767. Unsigned range is from 0 to 65535. The _size_ parameter specifies the maximum display width (which is 255) |
| MEDIUMINT(size) | A medium integer. Signed range is from -8388608 to 8388607. Unsigned range is from 0 to 16777215. The _size_ parameter specifies the maximum display width (which is 255) |
| INT(size) | A medium integer. Signed range is from -2147483648 to 2147483647. Unsigned range is from 0 to 4294967295. The _size_ parameter specifies the maximum display width (which is 255) |
| INTEGER(size) | Equal to INT(size) |
| BIGINT(size) | A large integer. Signed range is from -9223372036854775808 to 9223372036854775807. Unsigned range is from 0 to 18446744073709551615. The _size_ parameter specifies the maximum display width (which is 255) |
| FLOAT(size, d) | A floating point number. The total number of digits is specified in _size_. The number of digits after the decimal point is specified in the _d_ parameter. This syntax is deprecated in MySQL 8.0.17, and it will be removed in future MySQL versions |
| FLOAT(p) | A floating point number. MySQL uses the _p_ value to determine whether to use FLOAT or DOUBLE for the resulting data type. If _p_ is from 0 to 24, the data type becomes FLOAT(). If _p_ is from 25 to 53, the data type becomes DOUBLE() |
| DOUBLE(size, d) | A normal-size floating point number. The total number of digits is specified in _size_. The number of digits after the decimal point is specified in the _d_ parameter |
| DOUBLE PRECISION(size,d) | Equal to DOUBLE(size, d) |
| DECIMAL(size, d) | An exact fixed-point number. The total number of digits is specified in _size_. The number of digits after the decimal point is specified in the _d_ parameter. The maximum number for _size_ is 65. The maximum number for _d_ is 30. The default value for _size_ is 10. The default value for _d_ is 0. |
| DEC(size, d) | Equal to DECIMAL(size,d) |

#### Date and Time

Date and time data types for representing temporal values. Each temporal type has a range of valid values, as well as a "zero" value that can be used when you specify an invalid value that MySQL cannot represent.

| Data Type | Description |
|-----------|-------------|
| DATE | A date. Format: YYYY-MM-DD. The supported range is from '1000-01-01' to '9999-12-31' |
| DATETIME(fsp) | A date and time combination. Format: YYYY-MM-DD hh:mm:ss. The supported range is from '1000-01-01 00:00:00' to '9999-12-31 23:59:59'. Adding DEFAULT and ON UPDATE in the column definition to get automatic initialization and updating to the current date and time |
| TIMESTAMP(fsp) | A timestamp. TIMESTAMP values are stored as the number of seconds since the Unix epoch ('1970-01-01 00:00:00' UTC). Format: YYYY-MM-DD hh:mm:ss. The supported range is from '1970-01-01 00:00:01' UTC to '2038-01-09 03:14:07' UTC. Automatic initialization and updating to the current date and time can be specified using DEFAULT CURRENT_TIMESTAMP and ON UPDATE CURRENT_TIMESTAMP in the column definition |
| TIME(fsp) | A time. Format: hh:mm:ss. The supported range is from '-838:59:59' to '838:59:59' |
| YEAR | A year in four-digit format. Values allowed in four-digit format: 1901 to 2155, and 0000. MySQL 8.0 does not support year in two-digit format. |

#### Other Data Types

| Data Type | Description |
|-----------|-------------|
| sql_variant | Stores up to 8,000 bytes of data of various data types, except text, ntext, and timestamp |
| uniqueidentifier | Stores a globally unique identifier (GUID) |
| xml | Stores XML formatted data. Maximum 2GB |
| cursor | Stores a reference to a cursor used for database operations |
| table | Stores a result-set for later processing |

## INTEGRITY CONSTRAINTS

Integrity constraints in SQL are rules applied to database tables to maintain the accuracy, consistency, and validity of data, such as ensuring unique primary keys and valid foreign key relationships.

In essence, integrity constraints are crucial for:

- Preventing missing data
- Ensuring all data conforms to expected types and value ranges
- Maintaining proper links between data in different tables

Based on the example below, we will explain integrity constraints:

*Let's consider a relational database for a university. This database contains three tables: students, courses, and enrollments.*

### Students Table

The students table contains information about all university students.

- `student_id`: The student's identifier
- `first_name`: The student's first name
- `last_name`: The student's last name
- `email`: The student's email address
- `major`: The student's major
- `enrollment_year`: The year the student enrolled

### Courses Table

The courses table contains information about the courses available at the university.

- `course_id`: The course identifier
- `course_name`: The course name
- `department`: The course department

### Enrollments Table

The enrollments table stores information about which students are enrolled in which courses.

- `student_id`: The identifier of the student enrolled in the course
- `course_id`: The course identifier
- `year`: The enrollment year
- `grade`: The student's grade in that course
- `is_passing_grade`: A boolean indicating whether the grade is passing

### PRIMARY KEY Constraint

The university's goal is to uniquely identify each student. It is not advisable to use first and last name for this purpose due to the possibility of duplicate names among students. Similarly, relying on email addresses is not ideal, as students may change their emails.

The common solution is to assign a unique identifier to each student, stored in the `student_id` column. We can apply a PRIMARY KEY constraint to ensure each student has a unique identifier.

The PRIMARY KEY constraint ensures:
1. Each student has a `student_id`
2. Each `student_id` is unique

### Multi-column PRIMARY KEY Constraint

In certain scenarios, we need to use multiple columns to uniquely identify each row. A student can enroll in multiple courses, resulting in multiple rows sharing the same `student_id`. Similarly, a course can have multiple enrolled students.

Since no single field can uniquely identify a row, each enrollment record is determined using a combination of `student_id`, `course_id`, and `year`.

### Integrity Constraints After Table Creation

There are two ways to add integrity constraints. If the table already exists but you forgot to specify the PRIMARY KEY constraint, you can set it after the table is created using the ALTER TABLE command.

It is a best practice to name integrity constraints, as this provides several benefits:
- Allows for easier reference when modifying or removing constraints
- Supports management and organization of constraints

### NOT NULL Constraint

The university wants to ensure that each student's name and email are recorded in the database. NOT NULL constraints ensure that the `first_name`, `last_name`, and `email` columns cannot have NULL values.

### UNIQUE Constraint

Email addresses are inherently unique to each individual. In situations where a field should never have duplicate values, it is good practice to enforce this at the database level.

### Multi-column UNIQUE Constraint

Suppose you want to ensure that the course name for each department is unique in the courses table. In this case, the `course_name` and `department` columns together must be unique.

### NOT NULL UNIQUE vs. PRIMARY KEY Constraints

The difference between NOT NULL UNIQUE and PRIMARY KEY in a table is the purpose and intended use.

While both enforce uniqueness and non-nullability on one or more columns:
- A table can only have one PRIMARY KEY, which identifies each record
- A table can have any number of NOT NULL UNIQUE constraints for other important attributes

### DEFAULT Constraint

Students may need time after enrolling to select their major. The university would like the value of the major column to be "Undeclared" for students who haven't selected their major yet.

### CHECK Constraint

At this university, grades range from 0 to 100. A CHECK constraint can enforce that values are between 0 and 100.

CHECK constraints can involve more than one column. For example, we can ensure that `is_passing_grade` is TRUE if and only if the grade is at least 60.

### Types of CHECK Conditions

- **Range Conditions**: Ensure values are within a specific range
- **List Conditions**: Validate if a value matches a value in a specific list
- **Comparison Conditions**: Ensure values meet specific conditions (greater than, less than, etc.)
- **Pattern Matching Conditions**: Use pattern matching to validate text data
- **Logical Conditions**: Use logical operators (AND, OR, NOT)
- **Compound Conditions**: Apply conditions across multiple columns

### FOREIGN KEY Constraint

Foreign key constraints link the columns of two tables, ensuring referential data integrity. A foreign key in one table points to a primary key in another table, indicating that rows in those two tables are related.

In our example, each record in the enrollments table refers to a student and a course through the `student_id` and `course_id` columns, respectively. For them to be foreign keys, they must be primary keys in the students and courses tables.

## LOGICAL EXAMPLE

```sql
CREATE TABLE DATA
(
    CPF INT,
    DATE_OF_BIRTH INT,
    REGISTRATION_NUMBER INT PRIMARY KEY,
    DATE_OF_HIRE INT,
    DATE_OF_TERMINATION INT,
    NAME INT,
);

CREATE TABLE EMPLOYEES
(
    REGISTRATION_NUMBER INT,
    JOB_TITLE INT,
);

CREATE TABLE POSITION
(
    LEVEL INT,
    SALARY INT,
    JOB_TITLE INT PRIMARY KEY,
);

CREATE TABLE HISTORY
(
    SALARY_PROGRESSION INT,
    JOB_TITLE INT,
);

ALTER TABLE EMPLOYEES ADD FOREIGN KEY(REGISTRATION_NUMBER) REFERENCES DATA (REGISTRATION_NUMBER);
ALTER TABLE EMPLOYEES ADD FOREIGN KEY(JOB_TITLE) REFERENCES POSITION (JOB_TITLE);
ALTER TABLE HISTORY ADD FOREIGN KEY(JOB_TITLE) REFERENCES EMPLOYEES (JOB_TITLE);

CREATE VIEW EMPLOYEE AS
SELECT DATA.CPF, DATA.DATE_OF_BIRTH, DATA.REGISTRATION_NUMBER, DATA.DATE_OF_HIRE, 
       DATA.DATE_OF_TERMINATION, DATA.NAME, POSITION.LEVEL, POSITION.SALARY, 
       HISTORY.SALARY_PROGRESSION
FROM DATA;
-- Note: The original VIEW definition seems incomplete (missing JOINs)

CREATE VIEW HR AS
SELECT DATA.CPF, DATA.DATE_OF_BIRTH, DATA.REGISTRATION_NUMBER, DATA.DATE_OF_HIRE, 
       DATA.DATE_OF_TERMINATION, DATA.NAME, POSITION.LEVEL, POSITION.SALARY, 
       POSITION.JOB_TITLE, HISTORY.SALARY_PROGRESSION
FROM DATA;
-- Note: The original VIEW definition seems incomplete (missing JOINs)
```

## REFERENCES

- https://www.datacamp.com/pt/tutorial/integrity-constraints-sql
- https://learn.microsoft.com/pt-br/sql/t-sql/functions/date-and-time-data-types-and-functions-transact-sql?view=sql-server-ver17
- https://dev.mysql.com/doc/
- https://www.alura.com.br/artigos/mysql-do-download-e-instalacao-ate-sua-primeira-tabela
- https://www.w3schools.com/sql/
- https://www.oracle.com/br/mysql/what-is-mysql/
- https://www.brmodeloweb.com/lang/pt-br/index.html
