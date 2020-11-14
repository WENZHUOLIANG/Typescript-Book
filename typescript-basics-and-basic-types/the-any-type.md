# The 'any' Type



| Type | Example | Description |
| :--- | :--- | :--- |
| **number** | 1, 5.4, -10 | All numbers, no differentiation between integers or floats |
| **string** | 'Hi', "Hi",  \`\` | All text values. |
| **boolean** | true, false | Just these two, no "truthy" or "falsy" values |
| **object**  | {age: 30} | Any Javascript object, more specific types {type of object} are possible |
| **Array** | \[1,2,3\] | Any Javascript array, type can be flexible or strict \(regarding the element types\) |
| **Enum** | enum {NEW, OLD} | Added by Typescript: Automatically enumerated global constant identifiers |
| **Any** | \* | Any kind of value, no specific type assignment |

{% hint style="info" %}
Any type basically like Vanilla Javascript - It asks Typescript not check the type
{% endhint %}

