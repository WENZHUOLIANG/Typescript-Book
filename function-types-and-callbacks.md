# Function Types & Callbacks

Since we are able to pass the function as a type, we can use it inside another function. We can define a anonymous function or pass a function.

```typescript
function addAndHandle(n1: number, n2: number, cb: (num: number) =>  void) {
    const result = n1 + n2;
    cb(result);
}

addAndHandle(1,2, (result) => {
    console.log(result);
});


addAndHandle(1,2, printResult);
```



