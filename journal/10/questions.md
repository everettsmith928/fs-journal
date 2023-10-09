# CSharp and SQL Fundamentals
01. What is the purpose of a `namespace`?

  > | namespace allows you to control the scope of your classes and methods within them. |

02. What is the difference between a `class` and an `interface`?

  > | class is a blueprint for creating objects. Interface is a group of related properties and methods that describe an object. An interface only has a definition.  |

03. What is the method that returns an instance of a class, yet it has no return type?

  > | void |

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

  > | public |

06. In the Car example what is `string` an indication of?

  > | the value type that gets returned by the method |

07. In the Car example what is `abstract` preventing?

  > | It prevents the class from being modified, and derived classes should have all of their properties.  |

08. In a SQL table, what is the difference between information in a row and information in a column?

  > | Data in a row contains information that describes a single entity, while data in a column describes a field of information all entities possess. |

09. Demonstrate the necessary SQL for creating a table called `characters` with the values `name, age, description` as strings, and an `int` id.

  > | CREATE TABLE characters {
    name varchar(255),
    age int,
    description varchar(255).
    id int
  } |

10. In SQL how can you query more than a single table? Provide an example.

  > | the join operator.
  SELECT Orders.OrderID, Customers.CustomerName, Orders.OrderDate
  FROM Orders
  INNER JOIN Customers ON Orders.CustomerID=Customers.CustomerID;
  |
