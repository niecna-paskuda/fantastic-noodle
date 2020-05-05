---
description: Revising JavaScript
---

# JS

## Reading

### Books

* [ ] [https://github.com/getify/You-Dont-Know-JS](https://github.com/getify/You-Dont-Know-JS)

### List of books

* [ ] [https://exploringjs.com/](https://exploringjs.com/)
* [ ] [https://medium.com/javascript-scene/12-books-every-javascript-developer-should-read-9da76157fb3](https://medium.com/javascript-scene/12-books-every-javascript-developer-should-read-9da76157fb3)
* [ ] [https://medium.com/javascript-scene/how-to-learn-es6-47d9a1ac2620](https://medium.com/javascript-scene/how-to-learn-es6-47d9a1ac2620)
* [ ] [https://wsvincent.com/best-javascript-books/](https://wsvincent.com/best-javascript-books/)
* [ ] [https://gist.github.com/getify/7ae82fdc2e86bf66bcba](https://gist.github.com/getify/7ae82fdc2e86bf66bcba)

### Online courses

* [x] [https://app.pluralsight.com/paths/skill/javascript-core-language](https://app.pluralsight.com/paths/skill/javascript-core-language)

### Other

* [ ] [http://es6-features.org/](http://es6-features.org/#Constants)

## Q&As

questions and answers while reading

## Notes

### vars vs lets

* `var` – function scoped; no error when tries to access before initialisation,
* `let` – block scoped; cannot be used if unknown, results in a `ReferenceError`
* `const` =&gt; like `var`
* function identifier =&gt; like `var`
* function argument identifier =&gt; like var? why not like let? even though the argument IS function scoped but is a function not a block?
* `try catch err` identifier =&gt; like `let`

### strict mode

* gives errors before the script is run e.g. 

  `SyntaxError: Duplicate parameter name not allowed in this context  
       at wrapSafe (internal/modules/cjs/loader.js:1063:16)     
       at Module._compile (internal/modules/cjs/loader.js:1111:27)`

* anything other than the comment/whitespaces makes the strict useless, e.g. a `;`

### comparing

JS doesn't provide structural equality comparison because it's almost intractable to handle all the corner cases.

* `===` 
  * identity equality , not structural equality
  * no type coercion
  * do not use to compare NaN meaning: `NaN === NaN => false` use `Number.isNaN` or more strict `Object.is()`
* `==`
  * type coercion \(also considers type of the compared values\)
  * coerces to numeric type
* `< > <= >=`
  * numeric comparisons, unless both sides are strings already, alphabetical comparison used then `"10" < "9" => true` 

### classes

* keywords: `class`, `extends`, `constructor`, `super`, `this`, `new`
* everything is public \(?\)

### modules

* wrapping function – referred to as well as `module factories`
* explicitly create the object and thus expose some methods as public

### ES modules

* keywords:  `export`, `import`, 
* file-based, no wrapping function
* singletons – each `import` gives reference

### Iteration

* iterator implements: `next` method which returns an object with `value` and `done` properties
* iterable allows to create an iterator instance, by implementing the `Symbol.iterator()` and simply returning itself – single iterable can be consumed more than once, each time a new iterator instance is created
* 
