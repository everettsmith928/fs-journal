# Node

Express is a framework for node
sending requests through ports to receive and send files

send files depending on the request type

Middleware - logic built on our server for different requests(API KEY, FORMATTER, TURN INTO JS OBJECTS)
  Throughout our program to handle requests

Node Server Auth0 - only express server


Server:
  Where the controller and service go. MVC setup
  Controller: Tales in the actions from the User. Taking in our network requests(THE FIRST DOOR IN THE HALLWAY)
    Router - routing requests through express. all of the hallways.
    service is still responsible for altering data. There is no appstate. It is now the Database. 
    Middleman between the client and the database.

    Model is defined by Schema(MongoDB keyword) : Same as creating a class in the database. Requirements are build into the database.

    Run the server at a local port

Client 
BaseController = configures all of the routing through the server

You have to relaunch the sever every time you make a change ****



This is how you create a route on your server
Controller setup : export class ExampleController extends BaseController{
    
    constructor(){
      super('Sign on the Door : api/cats') - runs the constructor of BaseController
      this.router // This is the small hallway off the big one
      (Here you list the type of CRUD methods you want to allow in your class)
      .get('', this.function(request, response, next) => console.log('running this function')) <== this is the route where a function will run
    }

// Request is an object representing the incoming req from a user.
// Response is an outgoing object we send to the requester/user/client
// next is how we kick people back into the hallway
    getExample(req, res, next) {
      res.send('You got cats') <== res is a HTTP CODE like 200/400/100
    }
}

logger.log(request/res/next) makes it show in the console. Only shows in a dev environment

You have to do a return on your service to send the data back to the controller

request.params.banana

colon is how we string interpolate on the route(creates the variable)
next(error) // sends the user back to the hallway (can be a redirect to another request)

main.js DbConnection.connect() = connects to mongo db. 
.env CONNECTION_STRING= mongodb+srv://everettmarslandsmith:3wa4RgXUEqYRICL8@testdatabase.0vaw8g0.mongodb.net/?retryWrites=true&w=majority

Postman - test out your API because a URL can only do a get request

You can do a post request through POSTMAN with raw JSON. Just set up the keys and values. then you will be able to see the requests on your server

import schema from mongoose

Max is really important on your database

Schema needs to be registered with the DATABASE . DbContext is where we will add 
  Cars = mongoose.model('Car', carSchema)

  const car = await dbContext.Cars.create(carData)
  return car

exporting a const of a schema in the model



