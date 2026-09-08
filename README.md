CREATE DATABASE IF NOT EXISTS demonai;
USE demonai;
CREATE TABLE employee(
id INT AUTO_INCREMENT PRIMARY KEY NOT NULL, name VARCHAR(20), email VARCHAR(40),gender ENUM('Male','Female','Others'),salary DECIMAL(20,3), date_of_birth DATE, created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP);
INSERT INTO employee (name,email,gender,salary,date_of_birth)
VALUES
('Rahul','rahul6745denom.com','Male','250000','2000-05-12'),
('Tilak','tilak8909denom.com','Male','100000','2002-08-10'),
('Roshni','roshnil964denom.com','Female','350000','2006-01-10'),
('Shruti','shruti8069idenom.com','Female','80000','2004-12-15'),
('Sakshi','sakshi8008demon.com','Female','350000','2002-07-28');

SELECT * FROM employee WHERE salary >=250000;
ALTER TABLE employee
MODIFY COLUMN gender ENUM('Male', 'Female', 'Other');

ALTER TABLE employee
ADD COLUMN phone VARCHAR (15),
ADD COLUMN city VARCHAR (100);

ALTER TABLE employeem
RENAME COLUMN phone TO mobile_number;
