# Working with Numbers, Strings & Booleans

### WHAT

* Number by default are all `float` type

```typescript
const number = 5; // 5.0
```

### HOW - Core Types In Action

```typescript
function add(n1: number, n2: number, showResult: boolean, phrase: string) {
    const result = n1 + n2;
    if(showResult) {
        console.log(phrase + result);
    } else {
        return result;
    }
}

const number1 = 5;
const number2 = 2.8;
const printResult = true;
const resultPhrase = 'Result is: ';

add(number1, number2, printResult, resultPhrase); // will print out Result is: 7.8
```



