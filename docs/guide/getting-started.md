---
outline: deep
---

## Installation
You can install this plugin via npm
```sh
npm install vue-nice-debug
```

## Usage
inside your vite.config.js
```js
import debugPlugin from 'vue-nice-debug';

export default defineConfig({
	...
	plugins: [
		...
		debugPlugin('.vue'),
	],
})
```

### Transformation
This plugin will transform the following code 
```js
function exampleFn(arg1, arg2){
	...
}
```
into following code
```js
function exampleFn(arg1, arg2){
	console.log( 'function call: ' + 'exampleFn(' + arg1 + arg2 + ')' )
	...
}
```
Your arguments will be printed only if they not of object type, hence strings, numbers, are all valid
If argument value is object, the argument name will be printed as it is.