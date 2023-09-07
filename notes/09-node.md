# Node

Express is a framework for node
sending requests through ports to receive and send files

send files depending on the request type

Middleware - logic built on our server for different requests(API KEY, FORMATTER, TURN INTO JS OBJECTS)
  Throughout our program to handle requests

Node Server Auth0 - only express server


Server:
  Where the controller and service go. MVC setup
  Controller: Takes in the actions from the User. Taking in our network requests(THE FIRST DOOR IN THE HALLWAY)
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

setting up the query in the get is a req.query - creates an object with the query key:value pair
send it to the service and then search the database with the query

Here's how you import an id from a different collection - {type: Schema.Types.ObjectId ref: `collection`}
Virtual Key - Syntax  in Value.js - append after the schema

then ExampleSchema.virtual('other category', {
  localField: 'exhibitId', : property that you are using to grab from foreign field
  ref:'Exhibit', : Collection that you are grabbing from
  foreignField: '_id', : the property that you are tying to grab off the other object
  justOne: true
})

To add the virtual to your object in your get request: await (databasecall)examples.populate('other category', 'key emoji')
  attaches to your object the reference object or properties on that object.
  
Restful API conventions
Client should not have to format the query: we set that up on the server
.get('/:exhibitId/animals') - order of Dependency of Collections
dbContext.Examples.find({key: value}) or ({exhibitId}) if the key and value are the same JS uses it for both

Pipe operators do not work with truthy/falsy statements. You need to use a ternary operator

Many to Many has a middleman Object that keeps track of the relationships between 2 objects that don't know each other.

So we dont trust ownership from the client
We have to use the bearer token to check if the payload is actually coming from the User

.use(req,res,next) => you have to go through the use to get to the post
.use(Auth0Provider.getAuthorizedUserInfo) - needs to be at the top of where you need to be logged in to do the actions: appends the user object to your req
.post...
.get....

in network tab of dev tools: token - access_token: copy value and add it to the Authorization tab in Postman. This is how we attach the bearer token to our postman requests and gets attached, then validated through the use.