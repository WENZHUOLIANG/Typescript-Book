---
description: >-
  Focus on the WHY - Javascript does type assignment and checking in runtime
  while Typescript does that in static time.
---

# Typescript Types vs Javascript Types

### WHY - The comparison between JS and TS explains

```typescript
function add(n1: number, n2: number) {
    if(typeof n1 !== 'number' || typeof n2 !== 'number') {
        throw new Error('Incorrect Input!');
    }
    return n1 + n2;
}
```

Javascript is dynamically typed which means it's perfectly fine that we have a variable which initially might hold a number where we later assign a string into it. And that's why we have the type of operator so that we can check the current type of something at runtime.

Typescript, on the other hand, is statically type which means we define the type of variables and parameters ends on during development. They don't suddenly change during runtime.

{% hint style="info" %}
Javascript does understand the concept of types, it knows about some types like numbers, string, and boolean but using that always means that we can only fail at runtime instead of during development which is a better place for us as a developer.
{% endhint %}

{% hint style="info" %}
Javascript only knows couple of types, the way of checking in runtime is not as flexible or not as powerful as what we can do with Typescript.
{% endhint %}

