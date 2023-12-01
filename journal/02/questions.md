# Intro to JavaScript
01. Which keywords are used to declare a variable in JavaScript?

    > var, let, & const.

02. What is the definition of a function?

    > procedure designed to perform a specific task; something that takes an input and returns an output.

03. What are the `SOLID` principles?

    > Single-responsibility Principle, Open-closed Principle, Liskov Substitution Principle, Interface Segregation Principle, Dependency Inversion Principle

04. Given this array: How could you remove the `pineapple`?

    ```js
    let fruit = ['apple', 'banana', 'pineapple', 'orange', 'strawberry']
    ```

    > ```fruit.slice(2)``` - ".slice" should 'slice' the 3rd item in the array since arrays operate on [0,1,2,3,...etc.].

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

    > ```you.friends.push(them);``` & ```them.friends.push(you);```

06. Give an example of a JavaScript `Conditional`:

    > if (this) then (that). in JS you could say "if there are zero donuts, say 'someone ate my donuts!'" by using the following: ```If(donuts == 0){windows.alert('someone ate my donuts!')}```

07. What is the main difference between `parameters` and `arguments`?

    > parameters are variables that lack concrete values. arguments are the values passed around during invocations.

08. Instead of writing everything to the console, what is a better way to debug your code?

    > utilizing the debugger tool. better to let the tool jump you over to the problem then try and log every step yourself.

09. What is the difference between a `primitive` value and a `reference` value?

    > primitive operate directly on the equivalent of their value. reference operate more on their location in memory

10. Demonstrate a loop that prints the numbers between -100 and 100?

    > ```let text = "";
    > for (let i = -110; i < 101; i++) {
    >    text += i + "<br>";
    >}```
