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

Type aliases can be used to "create" your own types. You're not limited to storing union types though - you can also provide an alias to a \(possibly complex\) object type.

For example:

```typescript
type User = { name: string; age: number };
const u1: User = { name: 'Max', age: 30 }; // this works!
```

This allows you to avoid unnecessary repetition and manage types centrally.  
For example, you can simplify this code:

```typescript
function greet(user: { name: string; age: number }) {
  console.log('Hi, I am ' + user.name);
}
 
function isOlder(user: { name: string; age: number }, checkAge: number) {
  return checkAge > user.age;
}
```

To:

```typescript
type User = { name: string; age: number };
 
function greet(user: User) {
  console.log('Hi, I am ' + user.name);
}
 
function isOlder(user: User, checkAge: number) {
  return checkAge > user.age;
}
```

