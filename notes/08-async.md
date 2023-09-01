# Async

Allows your code to pause and wait for a line to return something. Based off of promises. Much like a promise in real life.

every promise has 2 arguments, resolve and reject is an (err). The code stops as soon as the error comes back. Doesn't run anything below it.

console.error(error)
Promises happen inside of a try catch usually

a promise is a class or object not a function.

API : Application Programming Interface

API all work a little bit differently

$ curl - grabs through the console.

Usually an API returns JSON, which we then have to parse

in your async getSomething() function:
  const response = await fetch(URL) replies with a promise object that holds the response
  console.log(response)
  const data = await response.json()
  console.log(data)

  In your network tab, select the fetch section and that will check your fetches. Then you can click on it to see the response or preview
  if we are returned an array we Map it to create each object

  AXIOS library
  <script axios> put above your app script tag
  
  const reponse = axios.get(URL)
  console.log(response.naming)

  auth0 : Domain : Audience: ClientID
    Environment files store our credentials
    generates a token for the user when they login : Bearer Token sent through the get request to return the userinfo object

    Payload is what we are sending to the API as a POST request

    Add locally with the response.data from the api

    Static: A method that exists on the class itself and is exported. must be invoked
    Getters: Exist on the instances of a class

    Account is stored in the appstate


  Don't import Axios 

  sandbox/api/category
  const api = axios.create({
    baseURL: API URL
      const response = await _sandboxApi.get('directory/subject')
  })

creator is an object stored on an object. Basically the user

Adapter Pattern = restructuring the data when you onstruct it through your class.

Flattening an object is removing the nested objects

Create: Post Method. Any time we do a post request we will supply a body. That's what gets sent to our API

enum : means it needs to have one of many selected values

Save a good form

Put Request: go find an object in the API and update the values. Add the ID to the URL for the PUT method
Resend the object through your class and then replace it in the APPSTATE array

How to recompile our SASS we just : this is after you modify all the colors in the variables.scss file
  NPM RUN SASS  --  Not Working

Axios is how we configure our base API urls and grab our requested data

create an instance of our api with AXIOS in our SErvice
  const dndapi = axios.create((
    baseURL: 'URL....',
    timeout: 5000,
    withCredentials: true : ONLY NECESSARY WHEN YOU NEED TO LOG IN TO THE API
  ))

  we may need to convert primitives from our API

  account is stored in the database. User is stored in Auth0
  if checking for a login using ('user') listener is faster

Query: sending specific requests to an API to retrieve specific data
API will require a key / password to show that you are authenticated

API key on your const apiReq = axios.create({
  params: {
  'key': 'value'
  }
})

onchange="" works for date pickers and selectable tables
