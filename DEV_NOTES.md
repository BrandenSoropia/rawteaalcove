# What is this?

Recording discoveries,thoughts, struggles etc while working on this project!

## August 1, 2022

### Global Styles

- Seems there isn't a documented way for global styles in SvelteKit.
- Random ways from Googling:

1. Global tag inside a random component
   Example:

```svelte
<style>
	:global(body) {
		/* this will apply to <body> */
		margin: 0;
	}
</style>
```

- This is hard to find.
- Seems kinda sketch to define in through this tag.

2. `__layout.svelte` + Global styles file
   Example:

```svelte
<script>
	import '../../static/global.css';
</script>
```

- Easier to find than 1)
- Should be familiar and one of the first place to look for global styles for those used to working with SvelteKit, since these layout files are hinted to be used for common UI stuff. ([Read more here](https://kit.svelte.dev/docs/layouts))
- [Pros/cons from this thread](https://github.com/sveltejs/kit/issues/3127)
  - Has access to SvelteKit preprocessing, so we can use SCSS etc to build our styles, then source it here.
  - Some find it weird to put **global** stuff here. I feel the same.

3. ✅ Vite + `global.css` file

- Liked this more since it keeps static files together. Probably not a good reason but I just liked the simplicity of importing 1 CSS file.
- Probably can also use some SCSS pre-processing via Vite if I really wanted to set that up.
- [Sourced from](https://www.closingtags.com/global-css-in-sveltekit/)
