# Understanding Typescript Core Libs

In the `compilerOptions` there is an attribute called `lib` . This will tell what default library typescript knows. For example, considering the following App

```typescript
const button = document.querySelector('button')!;

button.addEventListener('click', () => {
    console.log('Click!');
});
```

In Vanilla Javascript, of course it will work. However, when we write Typescript, it will not really be in the browser. If we comment out the `lib` then it will by default enable all `es6` features - like the DOM objects. However, if we uncomment out the `lib` folder, then it will look up the library in the `lib` folder as its first priority. So the compilation will fail.

Including the following libs will allow you to get the same behavior of the default `es6` option -

```typescript
"lib": [
  "dom",
  "es6",
  "DOM.Iterable",
  "ScriptHost"
],   
```



