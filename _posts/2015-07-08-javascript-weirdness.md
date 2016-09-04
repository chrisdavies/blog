---
layout: post
title:  "JavaScript Weirdness"
date:   2016-07-08 11:20:00 -0000
categories: javascript
---

In the following code, foo will have the value of ‘bar’…

```js
var foo = (2323, 'baz', 'bar');
```

JavaScript is so weird. I saw this code today in a student’s work, and thought it would produce a syntax error. Nope. Just a weird, unexpected side effect, instead.