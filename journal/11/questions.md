# A bit more CSharp and SQL
1. What does ***inheritance*** accomplish for us in C#?

  > ***inheritance*** allows a class to utilize the properties, fields, and methods of another class.

2. How does ***member inheritance*** work in C#? Does a `Class` inherit all members of the base `Class`?

  > ***member inheritance*** makes the derived class inherit all non-private members of its base class.

3. How does ***accessibility*** affect inheritance?

  > determines whether or not inheritance can occur (private or public/no access or access)

4. What is the difference between a `PRIMARY KEY` and a `FOREIGN KEY`

  > `PRIMARY KEY` column(s) that uniquely identifies each row in a table. 
  > `FOREIGN KEY` column(s) in a table that refers to the primary key in another table.

5. What is an ***alias***?

  > an alternative name for a table or column in a SQL query.

6. Demonstrate how you would query a join statement that would get all of a doctors patients from the following collections:

  ```SQL
  CREATE TABLE doctors (
    id INT NOT NULL AUTO_INCREMENT,
    -- CODE OMITTED
    PRIMARY KEY (id)
  )

  CREATE TABLE patients (
    id INT NOT NULL AUTO_INCREMENT,
    -- CODE OMITTED
    PRIMARY KEY (id)
  )

  CREATE TABLE patient_doctors (
    id INT NOT NULL AUTO_INCREMENT,
    doctorId INT NOT NULL,
    patientId INT NOT NULL,

    FOREIGN KEY (doctorId)
      REFERENCES doctors(id),
    FOREIGN KEY (patientId)
      REFERENCES patients(id),
  )

  ```

  > 
  ```SQL
  SELECT 
    patients.*
  FROM doctors
  INNER JOIN patient_doctors ON doctors.id = patient_doctors.doctorId
  INNER JOIN patients ON patient_doctors.patientId = patients.id
  WHERE doctors.id = chosenDoctorsId
  ```
