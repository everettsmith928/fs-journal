# Application Architecture, MVC Design Pattern
01. What are the Pillars of Object Oriented Programming (`OOP`)?
  
  > | Data Abstraction, Inheritance, Polymorphism, and Encapsulation 
      Data Abstraction: wrapping up complex actions into simple verbs. Hide the complexity.
      Inheritance: As much as you can the child class will inherit as much of the parent as possible. But will not be equal.
      Encapsulation: As much as you can, keep state and logic internal.
      Polymorphism: This basically means that we can call the same method on different objects.
  |

02. How does `export` differ from `export default`?
  
  > |Export multiple values as named exports with export. Export default exports a single value |

03. What is Encapsulation?
  
  > | As much as we can we want to keep state and logic internal. Where are responsibilities separate? Bundling data and the action that we want to use on that data together.
  
  Brenden Eich - Built Javascript

  The Gang of Four that Wrote Design Patterns
  Erich Gamma
  Richard Helm
  Ralph Johnson
  John Vlissides |

04. What are some of the benefits of the `Proxy` object that we are using in our structure for applications?
  
  > |This is the middleware between Javascript objects. Provide custom functionality to basic operations that can be performed on an object. We are using the Proxy object in our application as a sort of event listener. That detects when variables are reassigned. Meaning that we don't have to call our draw functions any time that we modify some data in the Appstate. Instead it will be detected or we can emit to the listener. |

05. What the difference between a `class` and an instance of a `class`?
  
  > | A class is the blueprint of an object that is build with the object constructor. Like a factory. While an instance of a class is the object built by calling that constructor. |

06. What is a computed Property?
  
  > | It's a property that's value is calculated using other stored values. |

07. What is the purpose of the `MVC` pattern?
  
  > | To modulate out our logic and code. Encapsulation is important in mvc. |

08. What is the job of the `Controller` in the `MVC` Pattern?
  
  > | The controllers job is writing to the DOM, taking in user input, handles the request flow. |

09. What is the job of the `Service` in `MVC`?
  
  > | The Service is where we use functions to manipulate data in the Appstate. |

10. What is the job of the `Model` in `MVC`?
  
  > | It is a blueprint of our data. And handles the logic of that data. |
