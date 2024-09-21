# learnsql
SQL practice and basic queries will be added here

https://www.sql-practice.com/

## SQL SELECT Statement

SELECT * FROM patients;
SELECT first_name, last_name FROM patients;

## SQL INSERT Statement

-- Insert data in all columns, mentioning column name is not required
// INSERT INTO tablename
    VALUES (value1, value2, value3, ...);

-- Insert a record
INSERT INTO patients (first_name, last_name, gender, birth_date, city, province_id, allergies, weight, height)
    VALUES ('John', 'Smith', 'M', '1994-02-21', 'Hamilton','ON', NULL, 132, 182);
 
-- Select the most recent record by id to display it.
select * from patients
    where patient_id = (select max(patient_id) from patients);

## SQL DELETE Statement

// DELETE FROM tablename WHERE condition;

DELETE FROM patients WHERE first_name = 'Paul';

-- There are no longer any patients named 'Paul' in the database
select * from patients where first_name = 'Paul'

## SQL UPDATE Statement

// UPDATE tablename
    SET column1 = value1, column2 = value2, ...
    WHERE condition;

UPDATE patients
SET
  first_name = 'John',
  weight = 120
WHERE patient_id = 1;

-- display the patient we just updated
select * from patients where patient_id = 1

// UPDATE Multiple Records 

--The following SQL statement will update the allergies to 'NKA' (no known allergies) for all records where allergies is NULL

UPDATE patients
SET allergies = 'NKA'
WHERE allergies is NULL;

-- display the patients table
select * from patients;

-- Changing first name
UPDATE patients 
SET first_name = 'SABBIR'
WHERE first_name - 'John";

## SQL WHERE Clause

SELECT * FROM patients WHERE gender = 'F';

-- Number fields require no quotes
SELECT * FROM patients WHERE patient_id=1;

### Operators

-- Equal, =
SELECT * FROM patients WHERE patient_id = 1;

-- Greater Than, >
SELECT * FROM patients WHERE patient_id > 5;

-- Less Than, <
SELECT * FROM patients WHERE patient_id < 5;

-- Greater Than Or Equal To, >=
SELECT * FROM patients WHERE patient_id >=5;

-- Less Than Or Equal To, <=
SELECT * FROM patients WHERE patient_id <= 5;

-- Not Equal, <> or != depending on sql version
SELECT * FROM patients WHERE patient_id <> 5

-- Between, inclusive range
SELECT * FROM patients WHERE patient_id BETWEEN 4 AND 6;

-- Like, pattern search
SELECT * FROM patients WHERE first_name LIKE 'a%';
  //First names starting with 'a'.
 //View sql patterns for more info.

 ![image](https://github.com/user-attachments/assets/dd7ff656-e42e-44b9-bea6-0c1b1a7f0b14)


-- In, in a collection
SELECT * FROM patients WHERE patient_id IN (1,3,6,9);
// the values can be replaced with a sub-query.
















