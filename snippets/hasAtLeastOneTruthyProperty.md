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
const objectTruthy = {
    check1: null,
    check2: null,
    check3: "This is a demo",
    check4: null
}

const objectFalsy = {
    check1: null,
    check2: false,
    check3: "",
    check4: null
}

hasAtLeastOneTruthyProperty(objectTruthy); // true
hasAtLeastOneTruthyProperty(objectFalsy); // false
```
