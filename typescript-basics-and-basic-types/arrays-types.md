# Arrays Types

## WHAT - what is arrays types

| Type | Example | Description |
| :--- | :--- | :--- |
| **number** | 1, 5.4, -10 | All numbers, no differentiation between integers or floats |
| **string** | 'Hi', "Hi",  \`\` | All text values. |
| **boolean** | true, false | Just these two, no "truthy" or "falsy" values |
| **object**  | {age: 30} | Any Javascript object, more specific types {type of object} are possible |
| **Array** | \[1,2,3\] | Any Javascript array, type can be flexible or strict \(regarding the element types\) |

When we define the array, Typescript will automatically infer the type from the element

```typescript
const person = {
    name: 'Wen',
    age: 30,
    hobbies: ['Sport', 'Music']
}

for(const hobby of person.hobbies) {
    console.log(hobby.toUpperCase());
}
```

