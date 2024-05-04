# About Object Oriented Paradigm(OOP)
  - C++ is an object-oriented programming language.
    
      1. Everything within a C++ program is an objects
  ## Principles's of OOP :
    1. Encapsulation : Encapsulation is a way to restrict the direct access to some components of an object, 
    so users cannot access state values for all of the variables of a particular object. Encapsulation can 
    be used to hide both data members and data functions or methods associated with an instantiated class 
    or object.

    2.Abstraction : Abstraction in OOPS is used to hide unnecessary information and display only necessary 
    information to the users interacting. It is essential to represent real-world objects in a simplified 
    manner for users to interact easily

    3.Inheritance : Inheritance is a mechanism that allows a class to inherit properties and behaviors 
    from another class. It is a fundamental concept in OOP that promotes code reuse and establishes 
    relationships between classes

    4.Polymorphism : Polymorphism is one of the core concepts in OOP languages and describes the concept
    of using different classes with the same interface. In other words, It is the ability of objects to 
    take on different forms or behave in different ways depending on the context in which they are used.

  ## Two Types of objects exists :
    - Fields: Store Data
    - Procedure: Store code
    

  ## Args vs Kwargs
    - Args : It is stands for arguments that are passed to the function
    - Kwagrs : It stands for keyword arguments which are passed along with the values into the functions

  ## Python Class and Object
  - Data hiding using private attributes using underscore as the prefix i.e single _ or double __

            class Parrot:
        
            // class attribute
            name = ""
            age = 0
          
        // create parrot1 object
        parrot1 = Parrot()
        parrot1.name = "Blu"
        parrot1.age = 10
        
        // create another object parrot2
        parrot2 = Parrot()
        parrot2.name = "Woo"
        parrot2.age = 15
        
        access attributes
        print(f"{parrot1.name} is {parrot1.age} years old")
        print(f"{parrot2.name} is {parrot2.age} years old")
    
        // Output: 
        Blu is 10 years old
        Woo is 15 years old


  ## Python Inheritance

    // base class
    class Animal:
        
        def eat(self):
            print( "I can eat!")
        
        def sleep(self):
            print("I can sleep!")
    
        // derived class
        class Dog(Animal):
            
            def bark(self):
                print("I can bark! Woof woof!!")
        
        // Create object of the Dog class
        dog1 = Dog()
        
        // Calling members of the base class
        dog1.eat()
        dog1.sleep()
        
        // Calling member of the derived class
        dog1.bark();
        
        Output 
        I can eat!
        I can sleep!
        I can bark! Woof woof!!

        // Here, dog1 (the object of derived class Dog) can access members of the base class Animal. It's because Dog is               inherited from Animal.

        // Calling members of the Animal class
        dog1.eat()
        dog1.sleep()


  ## Python Encapsulation
        class Computer:
      
          def __init__(self):
              self.__maxprice = 900
      
          def sell(self):
              print("Selling Price: {}".format(self.__maxprice))
      
          def setMaxPrice(self, price):
              self.__maxprice = price
      
      c = Computer()
      c.sell()
      
      // change the price
      c.__maxprice = 1000
      c.sell()
      
      // using setter function
      c.setMaxPrice(1000)
      c.sell()

      // Output
      Selling Price: 900
      Selling Price: 900
      Selling Price: 1000

      // In the above program, we defined a Computer class.

      // We used __init__() method to store the maximum selling price of Computer. Here, notice the code

      c.__maxprice = 1000

      // Here, we have tried to modify the value of __maxprice outside of the class. However, since __maxprice is a private variable, this modification is not seen on the output.

      // As shown, to change the value, we have to use a setter function i.e setMaxPrice() which takes price as a parameter.

  ## Python Polymorphism
      class Polygon:
        // method to render a shape
        def render(self):
            print("Rendering Polygon...")
    
    class Square(Polygon):
        // renders Square
        def render(self):
            print("Rendering Square...")
    
    class Circle(Polygon):
        // renders circle
        def render(self):
            print("Rendering Circle...")
        
    // create an object of Square
    s1 = Square()
    s1.render()
    
    // create an object of Circle
    c1 = Circle()
    c1.render()
    
    // Output
    Rendering Square...
    Rendering Circle...

    // In the above example, we have created a superclass: Polygon and two subclasses: Square and Circle. Notice the use of the render() method.

    // The main purpose of the render() method is to render the shape. However, the process of rendering a square is different from the process of rendering a circle.

    // Hence, the render() method behaves differently in different classes. Or, we can say render() is polymorphic.


# Python Flow Control
  ## Python if Statement
      An if statement executes a block of code only if the specified condition is met.
      Syntax: 
      if condition:
    // body of if statement
    Here, if the condition of the if statement is:
    
    True - the body of the if statement executes.
    False - the body of the if statement is skipped from execution.
    https://private-user-images.githubusercontent.com/51224267/327943960-76a6a503-aa1d-45bf-ba2f-d1fd7c82a431.PNG?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MTQ4MjE1MjQsIm5iZiI6MTcxNDgyMTIyNCwicGF0aCI6Ii81MTIyNDI2Ny8zMjc5NDM5NjAtNzZhNmE1MDMtYWExZC00NWJmLWJhMmYtZDFmZDdjODJhNDMxLlBORz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNDA1MDQlMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjQwNTA0VDExMTM0NFomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPWZlNzhhMTE1ZGM4YWFlYTllMjJkNmZkNTk3ZTNmOGYyN2EwYzg5N2FlZjRjOWMxYzlmZjQ3OWMyOTNjYWQ5NDcmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0JmFjdG9yX2lkPTAma2V5X2lkPTAmcmVwb19pZD0wIn0.tDeng4yRYT1sU_5eiqqh9Q9k44skazcjEFtQk4rWkho
