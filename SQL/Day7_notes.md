# SQL Constraints
SQL constraints are used to specify rules for data in a table.
The following constraints are commonly used in SQL:
   NOT NULL - Ensures that a column cannot have a NULL value
   UNIQUE - Ensures that all values in a column are different
   PRIMARY KEY - A combination of a NOT NULL and UNIQUE. Uniquely identifies each row in a table
   FOREIGN KEY - Prevents actions that would destroy links between tables
   CHECK - Ensures that the values in a column satisfies a specific condition
   DEFAULT - Sets a default value for a column if no value is specified
   CREATE INDEX - Used to create and retrieve data from the database very quickly

SQL NOT NULL on CREATE TABLE
CREATE TABLE Persons (
    ID int NOT NULL,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255) NOT NULL,
    Age int
);
SQL NOT NULL on ALTER TABLE
ALTER TABLE Persons
ALTER COLUMN Age int NOT NULL;

SQL UNIQUE Constraint
The UNIQUE constraint ensures that all values in a column are different.
CREATE TABLE Persons (
    ID int NOT NULL UNIQUE,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255),
    Age int
);
ALTER TABLE Persons
ADD UNIQUE (ID);

DROP a UNIQUE Constraint
To drop a UNIQUE constraint, use the following SQL:

MySQL:

ALTER TABLE Persons
DROP INDEX UC_Person;

SQL PRIMARY KEY Constraint
The PRIMARY KEY constraint is used to uniquely identify each record in a table.
CREATE TABLE Persons (
    ID int NOT NULL,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255),
    Age int,
    PRIMARY KEY (ID)
);
ALTER TABLE Persons
ADD CONSTRAINT PK_Person PRIMARY KEY (ID,LastName);

SQL FOREIGN KEY Constraint
The FOREIGN KEY constraint is used to prevent actions that would destroy links between tables.
CREATE TABLE Orders (
    OrderID int NOT NULL,
    OrderNumber int NOT NULL,
    PersonID int,
    PRIMARY KEY (OrderID),
    FOREIGN KEY (PersonID) REFERENCES Persons(PersonID)
);
ALTER TABLE Orders
ADD FOREIGN KEY (PersonID) REFERENCES Persons(PersonID);

ALTER TABLE Orders
DROP FOREIGN KEY FK_PersonOrder;

SQL CHECK Constraint
The CHECK constraint is used to limit the value range that can be placed in a column.
CREATE TABLE Persons (
    ID int NOT NULL,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255),
    Age int,
    CHECK (Age>=18)
);
ALTER TABLE Persons
ADD CHECK (Age>=18);


SQL DEFAULT Constraint
The DEFAULT constraint is used to set a default value for a column.

The default value will be added to all new records, if no other value is specified.

CREATE TABLE Persons (
    ID int NOT NULL,
    LastName varchar(255) NOT NULL,
    FirstName varchar(255),
    Age int,
    City varchar(255) DEFAULT 'Sandnes'
);

ALTER TABLE Persons
ALTER City SET DEFAULT 'Sandnes';

ALTER TABLE Persons
ALTER City DROP DEFAULT;














