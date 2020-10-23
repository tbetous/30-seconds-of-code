---
title: hasAtLeastOneTruthyProperty
tags: object,beginner
---

Check if an object has at least one property that is not falsy.

- Use `Object.keys` and `Array.some` to iterate on all properties of an object in order to find if at least one property is truthy.

```js
const hasAtLeastOneTruthyProperty = object => 
    Object.keys(object).some(key => {
        return object[key];
    });
```

```js
const formTruthy = {
    field1: null,
    field2: null,
    field3: "This is a demo",
    field4: null
}

const formFalsy = {
    field1: null,
    field2: null,
    field3: "This is a demo",
    field4: null
}

hasAtLeastOneTruthyProperty(formTruthy); // true
hasAtLeastOneTruthyProperty(formFalsy); // false
```
