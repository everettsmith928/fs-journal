# A bit more CSharp and SQL
1. What does ***inheritance*** accomplish for us in C#?

  > | Inheritance allows us to access methods of a parent class without modifying them. As well as extend upon the class without modifying the original in any way. |

2. How does ***member inheritance*** work in C#? Does a `Class` inherit all members of the base `Class`?

  > | Yes but you can only inheret from the Base Class and not a second one unelss you are using interfaces.|

3. How does ***accessibility*** affect inheritance?

  > | Accessibility means that certain instances are not accessible in a child class. But they can be nested within the parent class and then they are usable and inhereted.  |

4. What is the difference between a `PRIMARY KEY` and a `FOREIGN KEY`

  > | Primary key is the unique identification in a Table on a SQL database. The Foreign key is the unique identification on a seperate table than the first. |

5. What is an ***alias***?

  > | An alias is a variable version of a database table in sql. |

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

  > | SELECT FROM 
      patient_doctors.*,
      doctors.*
      JOIN patients ON patient_doctors
      WHERE doctors.id = patient_doctors.doctorId;
   |
