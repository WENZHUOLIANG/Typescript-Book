# Type Assignment & Type Inference

When the typescript code is converted into javascript code, the type is gone. That means, Javascript does not understand the syntax `n1:number` The reason why it is working is because the IDE understands typescript.

```javascript
function add(n1, n2) {
    return n1 + n2;
}
var number1 = 5;
var number2 = '2';
var result = number1 + number2;
console.log(result);
```

## WHAT - Type Inference

The following code is when we define a variable, we don't need to specifically define the type since Typescript is smart enough to understand the type

```typescript
const n1 = 5;
const n2 = 6;
const result = n1 + n2;

// no need to do
const n1: number = 5;
const n2: number = 6;
const result: number = n1 + n2;
```

{% hint style="info" %}
It is not a good practice to do `const n1: number = 5` since Typescript can automatically infer the type. 

But it is a good practice when you define the variable without assigning any values - like this `let n1: number`
{% endhint %}

