 Section 1: Data Insertion
 Task (1):- Create a database named CompanyDB.- Create a table `employees` with the fields: {name, ID, salary, skills, department_name, age}.- Insert multiple records into the table.- Use the `find()` method to verify the data:
  `db.employees.find()`
 Section 2: Relational Operators
 Task (2): - Find employees whose salary is greater than 50,000 using the `$gt` operator.
  Query:
  `db.employees.find({salary:{$gt:50000}})`
 Task (3): - Retrieve employees whose age is between 25 and 35 using `$gte` (greater than or equal to) and
 `$lte` (less than or equal to).
  Query:
  `db.employees.find({age:{$gte:25,$lte:35}})`
 Task (4): - Find employees in the IT department and sort them by age in descending order.
  Query:
  `db.employees.find({department_name:"IT"}).sort({age:-1})`
 Task (5): - Find employees whose names start with the letter 'A' or 'D' using the `$regex` operator.
  Query:
  `db.employees.find({name:{$regex:"^[AD]"}})`
 Section 3: Logical Operators
 Task (6): - Find employees who are either active or have a salary greater than 80,000 using `$or` and `$gt`.
  Query:
  `db.employees.find({$or:[{salary:{$gt:80000}},{status:"active"}]})`
 Task (7): - Retrieve employees not in the Sales department using `$ne` (not equal).
  Query:
  `db.employees.find({department_name:{$ne:"Sales"}})`
 Task (8): - Find employees who have both the skills "Communication" and "Presentation" using the `$all`
 operator.
  Query:
  `db.employees.find({skills:{$all:["Communication","Presentation"]}})`
 Section 4: Array Methods
Task (9): - Retrieve employees who have "MongoDB" listed as one of their skills.
  Query:
  `db.employees.find({skills:"MongoDB"})`
 Task (10): - Find employees with at least 3 skills in their `skills` array using the `$size` operator.
  Query:
  `db.employees.find({skills:{$size:3}})`
 Task (11): - Add a new skill "Leadership" to the skills array of Ishaan Gupta using `$push`.
  Query:
  `db.employees.updateOne({name:"Ishaan Gupta"},{$push:{skills:"Leadership"}})`
 Task (12): - Remove "MongoDB" from Ishaan Gupta's skills array using `$pull`.
  Query:
  `db.employees.updateOne({name:"Ishaan Gupta"},{$pull:{skills:"MongoDB"}})`
