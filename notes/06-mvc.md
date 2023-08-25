# MVC

Models VIews Controllers

Design Patterns : 
16 overall design patterns

Model : Blueprint of the data in the appstate
Views: visual data
Controller: available actions for the user and storing them


Encapsulation : developing all of the layers with single responsibility

Appstate: Where you store all of the data
  Import our Class and Contructor

bcw create

Learn SASS

node Modules;
Data 
Interactions and 
sLogic

npm

import {variable as entire JS file} from ".../.../..js"
import TAB when the file is open to get an auto gen IMPORT

Class : definition of what an object will look like/blueprint of what you want to make

Constructor : Runs anytime you build a new class. Parameters are in the scope of the function

export class Example{
  name 
  role
  health
  maxHealth

  constructor(newName, newRole, newHealth, newMaxHealth) {
  this.name = newName
  this.role = newRole
  this.health = newHealth
  this.maxHealth = newMaxHealth
  }
  
  method() {
    console.log(`hello I am` this.name)
  }

}

This goes into your Appstate
characters = {
  new Character(name, role, health, maxHealth)
  new Character(name, role, health, maxHealth)
  new Character(name, role, health, maxHealth)
}

Controller: CharactersController.js
export class CharactersController {
  Everything will be inside of this class and exported out as the class
  constructor(
    
  )
}

You can't access your objects form the Console
this = object looking at itself or own instance. When an object needs to reference it's own properties
let created = new Example()

Router in charge of new Controllers. Thats why we dont use new

created.property = access the properties of the object : accessing the object from the outside

First Model, then Appstate, then draw 

Scare Lewis - Friday: SpaceBar

Listener: Waits for a change in the Appstate(target) and changes the content based on a change happening

its like a bouncer outside of the Appstate that will notify when the selected prop(created variables within the Appstate) doesn't exist, or a value moves in or out. This is where you will do your draw function every time.

You give it the function instructions that you want it to run when something changes inside of the Appstate

Target is the Appstate and the Prop is the variable that you are trying to change.

emojipedia

add role = button when you are using a div as a button

Store.js = write a function that does a saveState('Name of What I want to Store', Appstate.variable of what I want to Store)
          run a loadState in init that parses json back into an array that remakes the class
          the.myArray = loadState('name of local storage', [Variable])

          You can't save a class to local storage. So you have to put it back into the array.

wrap an object in your constructor as an object ((name, type, )) now your constructor only takes an object. This allows you to recover it from local storage.

How to handle Form Data 

private function: written above our class in the controller _exampleFunction()

use rows within form to build a bootstrap form with style and spacing

form onsubmit="function that gets called: app.carcontroller.example()"
controller is where all user input will go through.

form data is passed through as variables under NAME

for each input the name is:
put into input -----> name = "make" => exactly matches the key on your class object. Because the form creates an object.

in the function you want to =
-------> const form = window.event.target
const formData = {
  make: form.make.value
  model: form.model.value
}

written into utils as FormHandler
--------> const formData = getFormData(form)

you need to grab value off of a form input with the key. which is name="key"

Local storage save function is a private one.

Pop is for displaying errors and or alerts. if(pop.confirm()) { do the block of code}
