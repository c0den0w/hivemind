JSX plainly put is just HTML markup returned by a Javascript function. JSX is a syntax extension for JavaScript that lets you write HTML-like markup inside a JavaScript file, keeping rendering logic and content in the same place.

## The Rules of JSX 

### 1. Return a single root element 

To return multiple elements from a component, **wrap them with a single parent tag.**
```
<>
<h1>Hello there!</h1>
<p>How are you doing??</p>
</>
```
This empty tag is called a _[Fragment.](https://react.dev/reference/react/Fragment)_ Fragments let you group things without leaving any trace in the browser HTML tree.

JSX looks like HTML, but under the hood it is transformed into plain JavaScript objects. You can’t return two objects from a function without wrapping them into an array.

### 2. Close all the tags
JSX requires tags to be explicitly closed: self-closing tags like `<img>` must become `<img />`, and wrapping tags like `<li>oranges` must be written as `<li>oranges</li>`.

### 3. camelCase ~~all~~ most of the things!
JSX turns into JavaScript and attributes written in JSX become keys of JavaScript objects. In your own components, you will often want to read those attributes into variables. But JavaScript has limitations on variable names. For example, their names can’t contain dashes or be reserved words like `class`.

This is why, in React, many HTML and SVG attributes are written in camelCase. For example, instead of `stroke-width` you use `strokeWidth`. Since `class` is a reserved word, in React you write `className` instead.

### 4. Passing strings with quotes
When you want to pass a string attribute to JSX, you put it in single or double quotes.

### 5. Using curly braces: A window into the JavaScript world
JSX is a special way of writing JavaScript. That means it’s possible to use JavaScript inside it—with curly braces `{ }`.

### 6. Using “double curlies”: CSS and other objects in JSX
In addition to strings, numbers, and other JavaScript expressions, you can even pass objects in JSX. Objects are also denoted with curly braces, like `{ name: "Hedy Lamarr", inventions: 5 }`. Therefore, to pass a JS object in JSX, you must wrap the object in another pair of curly braces: `person={{ name: "Hedy Lamarr", inventions: 5 }}`.