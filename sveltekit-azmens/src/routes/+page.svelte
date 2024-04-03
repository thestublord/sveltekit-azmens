<script>
	import { onMount } from 'svelte';
	import Events from '../lib/components/events.svelte';
	import Video from '../lib/components/video.svelte';

	onMount(() => {
		// Set a CSS variable for the height
		document.documentElement.style.setProperty('--vh', `${window.innerHeight * 0.01}px`);

		// Listen for the resize event and update the height
		window.addEventListener('resize', () => {
			document.documentElement.style.setProperty('--vh', `${window.innerHeight * 0.01}px`);
		});
	});
</script>

<div class="wrapper">
	<div class="video">
		<Video />
	</div>

	<div class="breadcrumb2">
		<!-- Breadcrumb content goes here -->
	</div>

	<div class="breadcrumb"></div>

	<div class="breadcrumb2">
		<!-- Breadcrumb content goes here -->
	</div>

	<h1>Upcoming Events</h1>
	<div class="events-section"></div>
	<div class="content">
		<Events />
	</div>
</div>

<style>
	/* Adjustments to the styles */

	.breadcrumb2 {
		padding: 1px;
		background-color: #dddddd; /* Light grey background */
	}

	h1 {
		font-size: 2em; /* Default font size */
		margin-bottom: 20px; /* Add margin to the bottom */
	}

	.wrapper {
		display: flex;
		flex-direction: column;
		width: 100%;
		font-family: 'Arial', sans-serif;
	}

	.breadcrumb {
		padding: 3px;
		background-color: #30475e;
		height: auto; /* Set height to auto to accommodate the h1 tag */
	}

	.content {
		display: flex;
		flex-direction: column;
		align-items: center; /* Center children vertically */
		justify-content: space-between; /* Distribute space evenly between children */
	}

	@media screen and (max-width: 950px) {
		/* Adjust the parallax height for medium screens */
	}

	@media screen and (max-width: 600px) {
		/* Adjust the parallax height for smaller screens */
		h1 {
			font-size: 1.6em; /* Decrease font size */
		}
	}
</style>
