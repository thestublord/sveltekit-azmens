<script>
	import Header from '$lib/components/header.svelte';

	import { onMount } from 'svelte';
	import Toolbar from '../lib/components/toolbar.svelte';

	onMount(() => {
		document.body.style.display = 'flex';
		document.body.style.flexDirection = 'column';
		document.body.style.minHeight = '100vh';
	});
</script>

<div class="layout">
	<Header />
	<Toolbar />
	<main>
		<slot />

		<!-- Background overlay -->
		<div class="background-overlay"></div>
	</main>
</div>

<style>
	.layout {
		display: flex;
		flex-direction: column;
		min-height: 100vh;
	}

	main {
		flex-grow: 1;
		padding: 1rem;
		text-align: center;
		color: rgb(90, 9, 9); /* Set text color to white */
	}

	/* Adjustments to the background image */

	main::before {
		content: '';
		position: absolute;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
		background-color: #fff8e0; /* Add # before the color code */
		background-size: cover; /* Cover the entire container */
		background-position: center; /* Center the background image */
		opacity: 2; /* Opacity of the background image */
		z-index: -3; /* Ensure the background image is behind the overlay */
	}
</style>
