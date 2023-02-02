# Sveltekit Misc Notes

## Routing
- The folder routes contains the pages
- File based routing

src`
+page.svelte
> domain.com

src/documents
+page.svelte
> domain.com/documents

## App Layout
+layout.svelte

## PageData
src
+page.svelte 
+page.ts

+page.ts 
- Runs serverside and clientside 
- Sends data down to the page

+page.ts
```ts
import type { PageLoad } from './$types';

export const load = (({ params }) => {
	return {
		name: "James"
	};
}) satisfies PageLoad;
```

+page.svelte
```html
<script lang="ts">
	import type { PageData } from "./$types";
	export let data: PageData

</script>
```


## Data Fetching
src
+page.svelte 
+page.server.ts

- use:enhance

## Importing Components 
$lib

## Fun Tools
svelte.config.js
```js
const config = {
	...
	vitePlugins: {
		experimental: {
			inspector: true
		}
	}
	...
}
```
When running a development environment, press <kbd>ctrl</kbd>  + <kbd>shift</kbd>, select the element to edit, and click. 

## Link Prefetching
`data-sveltekit-prefetch` in an element makes the links get prefetched on mouse hover or touch. 
