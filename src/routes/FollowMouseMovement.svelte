<script lang="ts">
	// For now, keep mouse state local since outside components don't need to know about it atm.
	let coords = { x: 50, y: 50 };
	let size = 10;
</script>

<svg
	class={$$props.class}
	on:mousemove={(e) => {
		coords = { x: e.clientX - size, y: e.clientY - size };
	}}
	on:mousedown={() => {
		size = 30;
	}}
	on:mouseup={() => {
		size = 10;
	}}
>
	<circle cx={coords.x} cy={coords.y} r={size} />
</svg>

<style>
	svg {
		width: 100%;
		height: 100%;

		border-color: blue;
		border-radius: 4px;
		border-style: solid;
		border-width: 1px;
	}

	circle {
		fill: #ff3e00;
	}
</style>
