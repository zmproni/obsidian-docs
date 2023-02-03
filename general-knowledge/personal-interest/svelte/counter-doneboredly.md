# Sveltekit Counter Website
- hooks.server.js
Runs the code at the start of the server once, except for the handle() function. 

- +page.server.js
All code written here will run on the server. It is safe to use imports to sensitive files. 

- Aliases 
```js
...
const config = {
	alias: {
		$db: './src/db'
	}
	...
}
export default config;
```
Aliases defined in the `svelte.config.js` file now handle import errors. Used to have to add lines to `jsconfig.js` before. 

- luxon 
https://moment.github.io/luxon/#/?id=luxon
https://moment.github.io/luxon/#/zones
Date handling. 
Time zones management. 
Date additions and subtractions. 
And more. 

- Adapters
```js
import adapter from '@sveltejs/adapter-node';
...
const config = {
	adapter: adapter({ out: 'build' }),
	...
}
export default config;
```
Builds to a node server. 

- `import { ... } from '$env/static/private';`
Interesting env variable loading. 