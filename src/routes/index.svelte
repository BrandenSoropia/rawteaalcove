<script>
	import FollowMouseMovement from './FollowMouseMovement.svelte';
</script>

<section>
	<h1>Welcome to SvelteKit</h1>
	<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>
	<!-- TODO: Figure out how to make circle slowly, follow mouse. -->
	<!-- TODO: Figure out how to drop up to 3 squares -->
	<!-- TODO: Figure out how to direct circle to dropped squares on drop and in order -->
	<!-- TODO: Delete/clear visited drop site. Allow drops again-->
	<div class="container">
		<nav>
			<a href="#">Test 1</a>
			<a href="#">Test 2</a>
			<a href="#">Test 3</a>
		</nav>
		<FollowMouseMovement class="canvas" />
	</div>
</section>
<section>
	<h1>Welcome to SvelteKit</h1>
	<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>
	<!-- TODO: Figure out how to make circle slowly, follow mouse. -->
	<!-- TODO: Figure out how to drop up to 3 squares -->
	<!-- TODO: Figure out how to direct circle to dropped squares on drop and in order -->
	<!-- TODO: Delete/clear visited drop site. Allow drops again-->
	<div class="container">
		<nav>
			<a href="#">Test 1</a>
			<a href="#">Test 2</a>
			<a href="#">Test 3</a>
		</nav>
		<FollowMouseMovement class="canvas" />
	</div>
</section>
<section>
	<h1>Welcome to SvelteKit</h1>
	<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>
	<!-- TODO: Figure out how to make circle slowly, follow mouse. -->
	<!-- TODO: Figure out how to drop up to 3 squares -->
	<!-- TODO: Figure out how to direct circle to dropped squares on drop and in order -->
	<!-- TODO: Delete/clear visited drop site. Allow drops again-->
	<div class="container">
		<nav>
			<a href="#">Test 1</a>
			<a href="#">Test 2</a>
			<a href="#">Test 3</a>
		</nav>
		<FollowMouseMovement class="canvas" />
	</div>
</section>

<style>
	section {
		padding: 16px;
	}

	.container {
		height: 100%;
		width: 100%;
		position: relative;
	}

	nav {
		position: absolute;
		top: 50%;
		right: 50%;
	}

	/* Need to pass in styles here, otherwise the absolution position breaks?
Might have to do with how styles are compartmentalized to components? */
	.container :global('canvas') {
		z-index: -1;
		position: absolute;
		background-color: aqua;
	}
</style>
