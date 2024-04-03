<script>
	import { goto } from '$app/navigation';
	import Events from '../lib/components/events.svelte';
</script>

<div class="parallax">
	<video muted autoplay playsinline loop>
		<source src="Designhhjkjh.mp4" type="video/mp4" />
		<track kind="captions" src="captions.vtt" srclang="en" label="English" />
		Your browser does not support the video tag.
	</video>
</div>

<div class="content">
	<div class="breadcrumb">
		<h1>Upcoming Events</h1>
	</div>

	<div class="breadcrumb2">
		<!-- Breadcrumb content goes here -->
	</div>

	<div class="events-section"></div>

	<Events />

	<div class="breadcrumb1">
		<!-- Breadcrumb content goes here -->
	</div>

	<div class="button-container">
		<button on:click={() => goto('/calendar')} class="calendar-button">Go to Calendar</button>
		<button on:click={() => goto('/contact')} class="calendar-button">Contact</button>
		<button on:click={() => goto('/about')} class="calendar-button">About</button>
	</div>
</div>

<style>
	.parallax {
		position: fixed;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
		z-index: -1;
	}

	.parallax video {
		width: 100%;
		height: 100%;
		object-fit: cover;
	}

	.content {
		position: relative;
		z-index: 1;
		background: rgba(
			255,
			255,
			255,
			0.7
		); /* Add a semi-transparent background to the content for better readability */
	}
</style>
