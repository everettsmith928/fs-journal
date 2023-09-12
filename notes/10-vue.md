# Vue

we do stuff inside the SRC in vue starter.
Main is where our javascript starts. Loads App.vue and router.js

RegisterglobalComponents, anything we put in components gets registered

components = controller and a view combined
everything needs its own controller in a way

We can now write logic - vieewcontroller inside of the vue files. conditionals

@ is used for an event listener

v-if 

v-else

router-link is how we navigate in a SPA
dont code over 150 lines

we wrote '<script></script> inside the component: requires an export default {}

computed is our listener now. inside of our script tag
user: computed(() => Appstate.user

data driven applications)

vt = setup for a .vue page
we inject our components into eachother

Our pages our just our parent components
App.vue holds our header and footer

anything we use in the page we need to return.. we can inject into the html with {{}}
mustache syntax: {{}} - vue grabs the value automatically
we import ref to make something reactive
let health = ref(100)
halth.value--

property was accessed and was not defined. VARIABLE IS NOT IN THE EXPORT DEFAULT ON YOUR COMPONENT

YOU CAN ONLY MAKE OBJECTS REACTIVE - then it can be subscribed to.

in Appstate: 

how to draw components like a foreach loop 
  <Component v-for="item in []" : key="item.id" :foodItem="item" />

Props: parameters or objects in VUE

props:{
  foodItem: {type: Object, required: true} **This is the singular version of our array. What we need to use in our component
}

One-Way Data Binding: Data from our script and computed
Two-Way Data Binding: We can change the data from both sides

We can loop over an object as well as an array

Tuesday, September 12th

Creating a website that pulls from an API and render with VUe

VUE LifeCycle Hooks
onMounted() : brought into document
onUpdate() : changes made
onUnmounted() : removed from doc

So onMounted() is used to fire off a function when the page loads

prop : sets up the component to take in data from a parent component
The page is responsible to pass the data

put modal into the app.vue to bring it in

proxy objects get unwrapped in the template. so we don't need props. or .value in the template

data.genres?.map => Use the elvis operator to see if an object has that key to run a method on it.