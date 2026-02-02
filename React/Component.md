_Components_ are one of the core concepts of React. React lets you combine your markup, CSS, and JavaScript into custom “components”, **reusable UI elements for your app.** Just like with HTML tags, you can compose, order and nest components to design whole pages. 

```
<article>  
<h1>My First Component</h1>  
<ol>  
<li>Components: UI Building Blocks</li>
<li>Defining a Component</li>  
<li>Using a Component</li>  
</ol>  
</article>
```
if the above markup is returned by a Javascript function then that is a component and it can be used in the markup of other components like

```
function Profile() {
  return (
    <img
      src="https://i.imgur.com/MK3eW3As.jpg"
      alt="Katherine Johnson"
    />
  );
}

export default function Gallery() {
  return (
    <section>
      <h1>Amazing scientists</h1>
      <Profile />
      <Profile />
      <Profile />
    </section>
  );
}
```
The export default prefix is a standard JavaScript syntax (not specific to React). This syntax is called [[JSX]], and it lets you embed markup inside JavaScript.