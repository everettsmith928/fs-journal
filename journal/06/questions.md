# Single Page Applications with Vue
01. What is the entrypoint of an application?

  > | APP.VUE |

02. What is the difference between a vue `component` and `page`?

  > | A Page holds components inside of it. |

03. What is ***Component-Based Architecture***?

  > | Every component of a website has its own unique functions and styles, and partitions the website into workable components |

04. What are the three tags that make up a Vue component?

  > | Template, Script, Style |

05. What are ***lifecycle hooks***? What are lifecycle hooks used for?

  > | They are used to make reactive content appear or dissappear from the page as changes are made or loaded. |

06. Which component in Vue does the vue-router use to mount pages onto?

  > | Router-Link |

07. What is the difference between the `AppState` and the state object within a component?

  > | The Appstate is where we store all of our local data, and the state object contains all of your application level state.|

08. What is the responsibility of `Services` in our Vue projects?

  > | The services is the same as in the MVC, this is where we will handle all of our business logic. |

09. What are ***props*** and how are they used? Provide an example

  > | Props are proxy objects that we use to pass down through our components. They are passed from the parent to the child component. So when we iterate through an array we know what that object is going to look like when we draw our data to the page with vue |

10. What is the Vue method used to create watchable objects such as `state` or `AppState`?

  > | computed(() => appstate.thing) |
