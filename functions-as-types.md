# Functions as Types

We can define function as a type, so that a variable can be defined as a function and can be assigned with the function definition. Like follows, 

```typescript
function add(n1: number, n2: number) {
    return n1 + n2;
}

function printResult(num: number) : void {
    console.log('Result: ' + num);
}

printResult(add(1,2));

let combineValues: Function;

combineValues = add;
combineValues = printResult;

console.log(combineValues(8,8));
```

but there is a problem, Function is too generic, how do we define a clear Function Type. So we are using the lambda syntax -&gt; `(...<parameter>) => <return value>` to define the contract of the function. You could think this as the interface - not implementation.

```typescript
function add(n1: number, n2: number) {
    return n1 + n2;
}

function printResult(num: number) : void {
    console.log('Result: ' + num);
}

printResult(add(1,2));

// let combineValues: Function;
let combineValues: (n1: number, n2: number) => number;

combineValues = add;
combineValues = printResult;

console.log(combineValues(8,8));
```

