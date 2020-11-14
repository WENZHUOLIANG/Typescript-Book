# Type Aliases / Custom Types

We can use `type` keyword to give the aliases to the type and assign it. That will be cleaner

```typescript
type Cominable = number | string;
type ConversionDescription = 'as-number' | 'as-text';

function add(
    n1: Cominable, 
    n2: Cominable, 
    resultConversion: ConversionDescription) {
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

