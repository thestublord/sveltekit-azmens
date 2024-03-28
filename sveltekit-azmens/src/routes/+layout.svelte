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
<Toolbar />
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
	main {
		flex-grow: 1;
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
		position: relative; /* Default position for larger screens */
		z-index: 1; /* Ensure the header stays on top of other content */
	}

	@media (max-width: 900px) {
		.header {
			position: fixed; /* Fix the position at smaller screens */
			top: 0; /* Align to the top of the viewport */
			left: 0; /* Align to the left of the viewport */
			width: 100%; /* Take up the full width of the viewport */
		}
	}
</style>
