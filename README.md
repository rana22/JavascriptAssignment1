# JavascriptAssignment1

- inspect chrome or any browser


## Q1 Hoisting:


```
console.log(x);
var x = 5;
foo();
function foo() {
  console.log("Function foo is called");
}

```

Tasks:

- Explain the output of the code.
- Modify the code to remove the undefined or unexpected behavior by using let or const instead of var.

## Q2 Scoping:


```
function outerFunction() {
  let outerVariable = "I'm outside!";
  function innerFunction() {
    let innerVariable = "I'm inside!";
    console.log(outerVariable);
  }
  innerFunction();
  console.log(innerVariable);
}
outerFunction();

```

Tasks:

- What will the code output? Explain why the code behaves this way.
- Modify the code so that both variables (outerVariable and innerVariable) can be logged in the console without errors. (Hint: Think about scope and variable declarations).

## Q3 Asynchronous JavaScript:

```
console.log("Start");
setTimeout(function() {
  console.log("Timeout");
}, 1000);
console.log("End");

```

Tasks:

- Predict the order of the output and explain why.
- Write a simple program that demonstrates the difference between synchronous and asynchronous execution. You can use setTimeout, or any other asynchronous function, to demonstrate the difference.

## Q4 Promises:

```
let promise = new Promise(function(resolve, reject) {
  let success = true;
  if (success) {
    resolve("The promise was successful!");
  } else {
    reject("The promise failed.");
  }
});

promise
  .then(function(message) {
    console.log(message);
  })
  .catch(function(error) {
    console.log(error);
  });

```

Tasks:

- Explain how promises work and what the above code does.
- Modify the code to introduce a delay of 2 seconds before resolving or rejecting the promise using `setTimeout`.

## Q5 Combining Async/Await with Promises :
Write a function fetchData that simulates fetching data from a server using a promise. The function should:

-  Use setTimeout to simulate a 3-second delay before resolving the promise.
- Return a message like "Data fetched successfully!" when the promise is resolved.

Tasks:

- Use `async/await` to call the `fetchData` function and log the result after it completes.
- Handle any possible errors using `try/catch` in the `async` function.