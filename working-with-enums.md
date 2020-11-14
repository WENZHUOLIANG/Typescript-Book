# Working with Enums

Loosely related to the idea of tuple is the idea of having a couple of specific identifiers global constants you might be working within your app which you want to represent as numbers. But to which you want to assign a human readable label. And for that you have the enum type.

| Type | Example | Description |
| :--- | :--- | :--- |
| **number** | 1, 5.4, -10 | All numbers, no differentiation between integers or floats |
| **string** | 'Hi', "Hi",  \`\` | All text values. |
| **boolean** | true, false | Just these two, no "truthy" or "falsy" values |
| **object**  | {age: 30} | Any Javascript object, more specific types {type of object} are possible |
| **Array** | \[1,2,3\] | Any Javascript array, type can be flexible or strict \(regarding the element types\) |
| **Enum** | enum {NEW, OLD} | Added by Typescript: Automatically enumerated global constant identifiers |

Let's say I have a requirement to assign some specific role - like AUTHOR, MANAGER, not other values other than there roles. Assigning a number does not make sense while assigning a string makes sense but hard to remember.

Another way to handle that is like that, but the downside is that we could still assign any number to the role

```typescript
const ADMIN = 0;
const READ_ONLY = 1;
const AUTHOR = 2;

const person = {
    name: 'Wen',
    age: 30,
    hobbies: ['Sport', 'Music'],
    role: ADMIN
}
```

So the solution is to use ENUM type

```typescript
enum Role { ADMIN, READ_ONLY, AUTHOR };

const person = {
    name: 'Wen',
    age: 30,
    hobbies: ['Sport', 'Music'],
    role: Role.ADMIN
}
```

{% hint style="info" %}
As best practice, use UPPERCASE as the enum type
{% endhint %}

After compiling into js -

```javascript
var Role;
(function (Role) {
    Role[Role["ADMIN"] = 0] = "ADMIN";
    Role[Role["READ_ONLY"] = 1] = "READ_ONLY";
    Role[Role["AUTHOR"] = 2] = "AUTHOR";
})(Role || (Role = {}));
;
var person = {
    name: 'Wen',
    age: 30,
    hobbies: ['Sport', 'Music'],
    role: Role.ADMIN
};
```

That's the power of the enum and it's a great construct whenever you need identifiers that are human readable and have some mapped value behind the scenes.

