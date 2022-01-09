``CREATE TABLE employee (
  id INTEGER PRIMARY KEY,
  first_name VARCHAR(50) NOT NULL,
  email VARCHAR(100),
  birthdate DATE
); ``

`` Created data on Mockaroo`` <br>
``
-insert into employee (first_name, email, birthdate) values ('Thaxter', 'tmackall0@youtu.be', '1981-06-27'); `` <br>

``insert into employee (first_name, email, birthdate) values ('Benjamin', 'brummins1@delicious.com', '1946-08-11'); `` <br>


``select * from employee``<br>
##### -----------------------update------------------------------------
``UPDATE employee
SET first_name = 'tugba',
	email = 'tugba@yavuzcom'
WHERE id = 3
RETURNING *;``

``UPDATE employee
SET first_name = 'PATİKA'
WHERE email LIKE 'ps%'
RETURNING *;``


``UPDATE employee
SET email = 'tugbayavuz@yandex.com'
WHERE email LIKE 'tugba%'
RETURNING *;``

``UPDATE employee
SET first_name = 'tugba1'
WHERE id=3
RETURNING *;``

##### -----------------------delete------------------------------------
``DELETE FROM employee
WHERE id=5
RETURNING *;``

``DELETE FROM employee
WHERE first_name ILIKE 'c%'
RETURNING *;``

``DELETE FROM employee
WHERE email ILIKE 'tr%'
RETURNING *;``
