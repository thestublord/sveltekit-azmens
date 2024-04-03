<script>
	import Header from '$lib/components/header.svelte';
	import { onMount } from 'svelte';
	import Footer from '../lib/components/footer.svelte';
	import Svg from '../lib/components/svg.svelte';

	onMount(() => {
		// Set a CSS variable for the height
		document.documentElement.style.setProperty('--vh', `${window.innerHeight * 0.01}px`);

		// Listen for the resize event and update the height
		window.addEventListener('resize', () => {
			document.documentElement.style.setProperty('--vh', `${window.innerHeight * 0.01}px`);
		});
	});
</script>

<body>
	<div class="header" style="z-index: 2;">
		<Header />
	</div>
	<div class="layout">
		<main>
			<slot />

			<!-- Background overlay -->
			<div class="background-overlay">
				<Svg />
			</div>
		</main>
	</div>
	<div class="footer">
		<Footer />
	</div>
</body>

<style>
	body {
		display: flex;
		flex-direction: column;
		height: calc(var(--vh, 1vh) * 100); /* Change min-height to height */
	}

	.layout {
		flex: 1 0 auto; /* Allow the layout to grow and shrink, but not to base its size on its children */
	}

	.footer {
		flex-shrink: 0; /* Prevent the footer from shrinking */
	}
	/* Add the following styles */
	.background-overlay {
		position: fixed;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
		background-color: #516b77;
		opacity: 0.5;
		z-index: -1;
	}

	main {
		text-align: center;
		color: #222831; /* Set text color to white */
	}

	/* Adjustments to the background image */

	.footer {
		margin-top: auto;
	}

	.header {
		position: relative;
		z-index: 2; /* Ensure the header stays on top of other content */
	}
</style>
