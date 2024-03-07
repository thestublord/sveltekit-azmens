<script>
	import Header from '$lib/components/header.svelte';
	import Footer from '../lib/components/footer.svelte';
	import Main from '../lib/components/main.svelte';
	import { onMount } from 'svelte';

	onMount(() => {
		document.body.style.display = 'flex';
		document.body.style.flexDirection = 'column';
		document.body.style.minHeight = '100vh';
	});
</script>

<div class="layout">
	<Header />
	<main>
		<slot />
		<Main />
		<!-- Background overlay -->
		<div class="background-overlay"></div>
	</main>
	<Footer />
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
		color: white; /* Set text color to white */
	}

	/* Adjustments to the background image */

	main::before {
		content: '';
		position: absolute;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
		background-image: url('/images/pexels-tom-fisk-11419474.jpg'); /* Path to your background image */
		background-size: cover; /* Cover the entire container */
		background-position: center; /* Center the background image */
		opacity: 2; /* Opacity of the background image */
		z-index: -3; /* Ensure the background image is behind the overlay */
	}

	.background-overlay {
		position: absolute;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
		background-color: rgba(0, 0, 0, 0.5); /* Semi-transparent black background */
		z-index: -2; /* Ensure the overlay is behind the main content */
	}
</style>
