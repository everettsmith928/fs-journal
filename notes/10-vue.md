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

Wednesday, September 13th

Vue Router: 

return component: [ component ]

Pages: get registered with a router file - regular components do not
router-link :to="{name: 'Name on the Route'}" Name is on the route, not the name of the page component

const router = useRouter()
return >>>>
router.push({ name: 'Name' }) ====> this is use when you want to send the user somewhere automatically

gap only works if your content is nested in the column!
PAGES NEVER TAKE IN PROPS!!! =================>>>>>

FIRST
first set up our pages, then connect in the router, build your class for the first GET.

SECOND
Then we make our service file, build onmounted on our page and call the service, put variables in the appstate

THIRD
create our computed on the PAGE connected to the APPSTATE, Build our template on the Page, then v-for on the page.

FOURTH
Create a card component for the data, send it to the forLoop by building props, Then use the prop on the component tag. DATA bind in the v-for to show all cars.

FIFTH
Do the Design for your template on your component with some custom CSS, When you click on the card use the router to send to a details page. entire component is a router-link.

SIXTH
Setup a DETAILS page, connect in the router. /cars/:carId, Then add params: { carId: car.id} to send to the router so it goes to that URL, Each new page should handle getting new DATA so onmounted get object by ID, then we grab the ID from the URL with const route = useRoute(), route.params.bananaId, write get function for specific car. remove it from the appstate while awaiting the API call..

SEVENTH
create the template for the active car now to display a singular object's details. add a v-if so it only tries to load when there is an active in the appstate

EIGHTH
Create a form in the page. Use 2 way data binding on the form. write create form, setup our form and v-model, push it back into the appstate, then to send them to the page we do a router push and send the full new object back to the top function. use params: {exampleID: object.id} in the push, then add a delete button, and router push the user back to the home page.


THURSDAY September 14th

You can import an entire component
When you are applying to a STYLE you need to string interpolate in the computed
  coverImg: computed(() => `url(${props.project.coverImg})`)
  then in STYLE use v-bind(coverImg)

Slots: pass template into another template
  <slot name="examples">
    will display nested component
  </slot>

Your components can open and close like an element
  <Example>
    <template #body> <==== target the name on your nested component
    nested Component
    </template>
  </Example>

You can reuse components with nested components

We pass down props from the parent element to the children

put in your ref data
watchEffect(()=> {

})

