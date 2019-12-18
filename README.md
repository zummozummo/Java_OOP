# Java_OOP
basics of java and opps concepts
**S.O.L.I.D**
S — Single responsibility principle
O — Open closed principle
L — Liskov substitution principle
I — Interface segregation principle
D — Dependency Inversion principle


# Java_OOP
basics of java and opps concepts
**S.O.L.I.D DESIGN PRINCIPLES** 
S - Single Responsibility Principle (known as SRP)
O - Open/Closed Principle
L - Liskov’s Substitution Principle
I - Interface Segregation Principle
D - Dependency Inversion Principle

Single Responsibility
-------------------------
“class should be having one and only one responsibility”. What does it mean? 
A class or module should have only one reason to change.

What is Responsibility
Responsibility is the work or action that each part of your system, the methods, the classes, the packages, the modules are assigned to do.
Too much responsibility leads to coupling.

For example, lets say we have a User Class that we keep some info in there.
class User {
  public age;  
  public name;
  public slug;
  public email;
}

It does make sense to keep only methods that set or get the role, name, age properties.
However, if we decided to add some other methods:
class User {
  public age;  
  public name;
  public slug;
  public email;
  // Xmm why do we have them here?
  checkAge();
  validateEmail();
  slugifyName();
}



Well let’s take the class A which does the following operations.
1)Open a database connection
2)Fetch data from database
3)Write the data in an external file

The issue with this class is that it handles lot of operations. Suppose any of the following change happens in future.
The issue with this class is that it handles lot of operations. Suppose any of the following change happens in future.
•	New database
•	Adopt ORM to manage queries on database
•	Change in the output structure
So in all the cases the above class  would be changed. Which might affect the implementation of the other two operations as well. So ideally according to SRP there should be three classes each having the single responsibility.



Ex2- 
class 1-  EmployeePayroll
class2-EmployeeLeave
class3-EmployeTimeSheet    
as the above 3 classed are doing only 1 thing they all follow single responsibility principle, if in future you want to make some change you know where to make changes.
