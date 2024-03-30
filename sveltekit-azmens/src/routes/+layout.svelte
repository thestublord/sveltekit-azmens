<script>
	import Header from '$lib/components/header.svelte';
	import { onMount } from 'svelte';
	import Toolbar from '../lib/components/toolbar.svelte';
	import Footer from '../lib/components/footer.svelte';

	onMount(() => {
		document.body.style.display = 'flex';
		document.body.style.flexDirection = 'column';
		document.body.style.minHeight = '100vh';
	});
</script>

<div class="header" style="z-index: 2;">
	<Header />
</div>

<div class="layout">
	<main>
		<slot />

		<!-- Background overlay -->
		<div class="background-overlay"></div>
	</main>
</div>

<div class="footer">
	<Footer />
</div>

<style>
	/* Add the following styles */

	.layout {
		min-width: 400px; /* Prevent the main content from shrinking under 400px */
	}

	main {
		text-align: center;
		color: #dddddd; /* Set text color to white */
	}

	/* Adjustments to the background image */

	main::before {
		content: '';
		position: fixed;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
		background-color: #dddddd;
		background-size: cover;
		background-position: center;
		opacity: 0.5;
		z-index: -1;
	}

	.footer {
		margin-top: auto;
	}

	.header {
		position: relative;
		z-index: 2; /* Ensure the header stays on top of other content */
	}

	@media (max-width: 900px) {
		.header {
			position: fixed;
			top: 0;
			left: 0;
			width: 100%;
		}
	}
</style>
