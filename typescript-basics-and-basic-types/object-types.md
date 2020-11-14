# Object Types

### WHAT - what is object types

| Type | Example | Description |
| :--- | :--- | :--- |
| **number** | 1, 5.4, -10 | All numbers, no differentiation between integers or floats |
| **string** | 'Hi', "Hi",  \`\` | All text values. |
| **boolean** | true, false | Just these two, no "truthy" or "falsy" values |
| **object**  | {age: 30} | Any Javascript object, more specific types {type of object} are possible |

Let's look at the following sample code

```typescript
const person = {
    name: 'Wen',
    age: 30
}

console.log(person);
```

What I hover my mouse in the person - we are see the following. And indeed this is not a javascript object with a commas here. This is the object type inferred by Typescript and object types are written almost like objects.

![](../.gitbook/assets/image%20%282%29.png)

```javascript
const person: {
    name: string;
    age: number;
}
```

But the above example is auto assigned with a **generic** object type as equals as

```typescript
const person: object = {
    name: 'Wen',
    age: 30
}

console.log(person);
```

When I hover the mouse in the person in line 6, there is no help from the IDE since the IDE does not able to understand any specific type inside the generic object type. And we will also get the error when we try to access the attribute.

![](../.gitbook/assets/image%20%283%29.png)

To fix that, we will need to assign a specific object type - `{name: string; age: number}` Also you can see the IDE could defect the attribute from the type.

![](../.gitbook/assets/image%20%284%29.png)

But after compiling with `tsc app.ts` Javascript still has a plain object with no type. The type assignment just happens on the typescript, NOT javascript

```javascript
var person = {
    name: 'Wen',
    age: 30
};
console.log(person.name);
```



