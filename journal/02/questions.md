# Intro to JavaScript
01. Which keywords are used to declare a variable in JavaScript?

    > | const, let, var |

02. What is the definition of a function?

    > | A subprogram defined to accomplish a specific task |

03. What are the `SOLID` principles?

    > | SINGLE RESPONSIBILITY
        OPEN CLOSE PRINCIPAL
        LISKOV SUBSTITUTION PRINCIPAL
        INTERFACE SEGREGATION PRINCIPAL
        DEPENDENCY INVERSION PRINCIPAL |

04. Given this array: How could you remove the `pineapple`?

    ```js
    let fruit = ['apple', 'banana', 'pineapple', 'orange', 'strawberry']
    ```

    > | function removePineapple() {
        fruit.splice(fruit.indexOf('pineapple'), 1)
            
    } |

05. Given these two objects: How could you add each to the others friends arrays?

    ```js
    let you = {
        name: "You",
        hair: true,
        friends: []
    }
    let them = {
        name: "Them",
        hair: false,
        friends: []
    }
    ```

    > | you.friends += them.name
        them.friends += you.name |

06. Give an example of a JavaScript `Conditional`:

    > | if (variable.name > otherOne.name) {
        Execute this block of code
    }|

07. What is the main difference between `parameters` and `arguments`?

    > | Parameters are the temporary variable that is signed to the passed argument and used within the function. And an argument is what is passed into the function|

08. Instead of writing everything to the console, what is a better way to debug your code?

    > | Putting the debugger into your function can be very useful. Also talking out loud and telling a story about what your code is doing can help you identify the issue. |

09. What is the difference between a `primitive` value and a `reference` value?

    > | A primitive value can be a boolean, number, string, undefined, and null
    A reference data type is one that when cloned modifies the original object. Like an array or date.  |

10. Demonstrate a loop that prints the numbers between -100 and 100?

    > | for(let i = -100; i <= 100; i++) {
        console.log(i)
    } |
