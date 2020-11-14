# Union Types

If you want flexibility of type, you can use Union Types but you would need runtime check

Requirement: Develop a function which could handle combine two numbers and two string. If the input is number, then do mathematical addition; otherwise to do concatenation.

```typescript
function add(n1: number | string, n2: number | string) {
    let result;
    if(typeof n1 === 'number' && typeof n2 === 'number') {
        result = n1 + n2;
    } else {
        result = n1.toString() + n2.toString();
    }
    return result;
}

const combineAges = add(10,20);
console.log(combineAges);
const combineNames = add('Wen', 'Liang');
console.log(combineNames;)
```

