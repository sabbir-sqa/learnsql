## SQL AND, OR and NOT Operators

SELECT * FROM patients
WHERE first_name='Jon' AND city='Toronto';

SELECT * FROM patients
WHERE city='Hamilton' OR city='Toronto';

SELECT * FROM patients
WHERE NOT provience_id='ON';

## SQL ORDER BY Keyword

SELECT * FROM patients
ORDER BY first_name;

SELECT * FROM patients
ORDER BY first_name DESC;

SELECT * FROM patients
ORDER BY first_name, last_name;

SELECT * FROM patients
ORDER BY first_name ASC, last_name DESC;

## SQL LIKE Operator

SELECT * FROM Customers
WHERE first_name LIKE 'b%';