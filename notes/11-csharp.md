# CSharp

Postman Test 10/4

Socket is a messaging system between server and client
WS button in network tab

Socket_authenticated(received messages)
  red
  green: messages we send

  Socket Service and Handler(similar to controlller) tell us what to do when we receive a message, but dont respond

  only one type of send() == message 

  no async

  socketSErvivice.emit('SOCKET_TEST')

socketProvicder.message('USER_LOGGED_IN') == on the server

You can see any action on the server side from anywhere

Use a auth socket to queue up requests while you are waiting for authorization. Only sends when you are logged in.


10/9/2023

BAckend language - C#
Console.WriteLine()

every line ends with semi-colon: strict

numbers are integers data type matches var

INTEGER ACCURACY
float z = 4.5f; (used for a decimal number)
double a = 5.55;
decimal b = 6.70912m; (used for a money $)

STRINGS
string greeting = "hello";
char = 'a'; single quote for characters;

BOOLEAN
bool ok = true;
bool no = false;

ARRAYS
we probably dont use them, must have a declared length. We use list mostly instead

LIST
List<string> cats = new List<string>(){"Something", "Another"}; Works just like an array in javascript. NO LENGTH(COUNT)

cats.Add("gopher");
cats.Add("Bean");

OBJECTS
Don't really use them in C#

DICTIONARY
Dictionary<string, int> codeworksCats = new Dictionary<string, int>()
codeworksCats.Add("jeremy, 7")
codeworksCats.Add("Sam", 1);

 - Data type that takes in a key value pair


Debug Anyway runs the last working compiled version
Errors are stuck in the VS code until you recompile

// Memers are created with Capital Letters. Cars and Params are lowercase

class Cat{
  string Name;
  string Color:
  int Age;
  public Cat(string name, int age, string color) - this is the constructor
  {
    this.Age = age
    Name = name
  }
}

List<Cat> catsTheMovie = new List<Cat>();

bcw create dotnet-auth





Model - define how we want the object to look as we pass it, then build the schema out

You can provide an accessor - public (This can be used anywhere)

MODEL

namespace catRoundUp.Models;

class Cat{
  public int id;
  public string Name; - (Can change this)
  public string Color;
  public readonly int Age; - (Can't change the value)
  private bool Feisty;

    public Cat(int id, string name, string color, int age)
    {
      Id = id;
      Name = name;
      Color = color;
      Age = age;
      Feisty = feisty;
    }
}

https://localhost:7045
CONTROLLER

<!-- using catRoundUp.Models; - How you bring in classes from other files
using catRoundUp.Services; --> We have these globally accessed

[ApiController] - Decorators
[Route("api/cats")]
public class CatsController : ControllerBase{

  private readonly CatsService _catsService;
  public CatsController(CatsService cs) {
    _catsService = cs;
  }

[HTTPGet]
public ActionResult<List<Cat>> GetCats() {
  return "Hey it worked!";
  try
  {
    List<Cat> cats = _catsService.GetCats();
    return Ok(cats);
  }
  catch(Exception e.Message)
  {
    return BadeRequest(e.Message)
  }
}
}

SERVICE - Talks with the repository layer to grab things from the DB
namespace catRoundUp.Services
public class CatsService{
  private readonly CatsREpository _repo;
  internal List<Cat> GetCats()
  {
    List<Cat>
  }
}

REPOSITORY
namespace catRoundUp.Repositories;
public class CatsRepository{
  private List<Cat> _FakeDb;
  public CatsRepository()
  {
    _FakeDb = newList<Cat>();
    _FakeDb.Add(new Cat(1, "Something", "red", 10, true))
  }
}

We store our dependencies in out Startup.cs
The order is important here
  services.AddSingleton<CatsRepository>();
  services.AddScoped<CatsService>();

Function that doesn't return something has the void
