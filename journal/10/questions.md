# CSharp and SQL Fundamentals
01. What is the purpose of a `namespace`?

  > organization; prevents name collisions by separating your code into logical groups.

02. What is the difference between a `class` and an `interface`?

  > `class` describes the behavior of objects in a program. `interface` carries those behaviors.
  
03. What is the method that returns an instance of a class, yet it has no return type?

  > constructor

05. In the Car example what is the access modifier of the `Start()` method?

  ```c#
  abstract class Car
  {
    public string Start()
    {

      return "Vroooom";

    }
  }
  ```

  > public

06. In the Car example what is `string` an indication of?

  > the return type

07. In the Car example what is `abstract` preventing?

  > prevents the Car from being instantiated directly. It indicates that the class is incomplete and must be implemented by derived classes.

08. In a SQL table, what is the difference between information in a row and information in a column?

  > row represents a single instance of data; column represents a specific attribute of that data

09. Demonstrate the necessary SQL for creating a table called `characters` with the values `name, age, description` as strings, and an `int` id.

  > ```c#
  CREATE TABLE characters (
    id INT PRIMARY KEY,
    name VARCHAR(255),
    age VARCHAR(255),
    description VARCHAR(255)
  )
  ```

10. In SQL how can you query more than a single table? Provide an example.

  > you can query multiple tables with JOIN operations
  ```c#
  SELECT cars.model, cars.make, carCreator.name
  FROM cars
  INNER JOIN carCreator ON cars.id = carCreator.carId
  ```
