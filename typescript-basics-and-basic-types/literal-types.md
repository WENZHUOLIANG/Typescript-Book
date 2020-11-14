# Literal Types

The ENUM type allows developer can choose a particular human-readable type. Look at the following use case, I have a function that needs a third parameter to determine some logic

The following code represents how literal types work. It is similar to Enum type, but only limits to only two strings. 

```typescript
function add(
    n1: number | string, 
    n2: number | string, 
    resultConversion: 'as-number' | 'as-text') {
    let result;
    if(typeof n1 === 'number' && typeof n2 === 'number' || resultConversion === 'as-number') {
        result = +n1 + +n2;
    } else {
        result = n1.toString() + n2.toString();
    }
    return result;
}

const combineAges = add(10,20,'as-number');
console.log(combineAges);
const combineNames = add('Wen', 'Liang', 'as-text');
console.log(combineNames);
```

