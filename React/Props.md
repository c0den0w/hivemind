React components use _props_ to communicate with each other. Every parent component can pass some information to its child components by giving them props.

Props are the information that you pass to a JSX tag. For example, `className`, `src`, `alt`, `width`, and `height` are some of the props you can pass to an `<img>`

The props you can pass to an `<img>` tag are predefined. But you can pass any props to _your own_ components, such as `<Avatar>`, to customize them.

### Step 1: Pass props to the child component
First pass some props to the Avatar component.
```
export default function Profile() {  
	return (  
		<Avatar  
		person={{ name: 'Lin Lanying', imageId: '1bX5QH6' }}  
		size={100}  
		/>  
	);  
}
```

### Step 2: Read props inside the child component
You can read these props by listing their names `person, size` separated by the commas inside `({` and `})` directly after `function Avatar`. This lets you use them inside the `Avatar` code, like you would with a variable. This syntax is called [[destructuring]] and is equivalent to reading properties from a function parameter.
```
function Avatar({ person, size }) {  
// person and size are available here  
}
```

## Specifying a default value for a prop
If you want to give a prop a default value to fall back on when no value is specified, you can do it with the destructuring by putting `=` and the default value right after the parameter:

```
function Avatar({ person, size = 100 }) {  // ...}
```

