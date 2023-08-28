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