# Working with Tuples

### WHAT - what is turples type

| **number** | 1, 5.4, -10 | All numbers, no differentiation between integers or floats |
| :--- | :--- | :--- |
| **string** | 'Hi', "Hi",  \`\` | All text values. |
| **boolean** | true, false | Just these two, no "truthy" or "falsy" values |
| **object**  | {age: 30} | Any Javascript object, more specific types {type of object} are possible |
| **Array** | \[1,2,3\] | Any Javascript array, type can be flexible or strict \(regarding the element types\) |
| **Tuple** | \[1,2\] | Added by Typescript: Fixed-length array |

Look at the following code, I have an attribute called role, my requirement is that the role should have only 2 elements, however, defining as an array will not give this restriction.

```typescript
const person = {
    name: 'Wen',
    age: 30,
    hobbies: ['Sport', 'Music'],
    role: [2, 'author']
}
person.role.push('admin');
```

To fix that, typescript cannot auto infer the type. So we have to explicitly define the type as follows

```typescript
const person: {
    name: string;
    age: number;
    hobbies: string[];
    role: [number, string]
} = {
    name: 'Wen',
    age: 30,
    hobbies: ['Sport', 'Music'],
    role: [2, 'author']
}
```

```typescript
person.role.push('admin'); // this is special, still works
person.role[1] = 10; // this will throw error - Type 'number' is not assignable to type 'string'.
person.role = [2, 'author', 10]; // this will throw error - 
// Type '[number, string, number]' is not assignable to type '[number, string]'.
// Source has 3 element(s) but target allows only 2.
```

