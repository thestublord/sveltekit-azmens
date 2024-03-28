<script>
	import { goto } from '$app/navigation';
	import Events from '../lib/components/events.svelte';
	import Video from '../lib/components/video.svelte';
	import Calendar from '../lib/components/calendar.svelte';
	import Footer from '../lib/components/footer.svelte';
	import Homeimage from '../lib/components/homeimage.svelte';
	import Eventsimage from '../lib/components/eventsimage.svelte';
</script>

<div class="wrapper">
	<div class="video">
		<Video />
	</div>

	<div class="breadcrumb">
		<h1>Upcoming Events</h1>
	</div>

	<div class="breadcrumb1">
		<!-- Breadcrumb content goes here -->
	</div>

	<div class="events-section"></div>
	<div class="content">
		<Events />
	</div>

	<div class="calendar-section">
		<button on:click={() => goto('/calendar')} class="calendar-button">Go to Calendar</button>
	</div>
	<div class="parallax2"></div>
</div>

<style>
	/* Adjustments to the styles */

	.wrapper {
		display: flex;
		flex-direction: column;
		width: 100%;
	}
	.breadcrumb1 {
		padding: 2px;
		background-color: #f05454; /* Light grey background */
	}

	.parallax2 {
		background-image: url('/images/3.png');
		height: 810px;
		background-attachment: fixed;
		background-position: center;
		background-repeat: no-repeat;
		background-size: cover;
	}

	.breadcrumb {
		padding: 20px;
		background-color: #30475e; /* Light grey background */
		height: auto; /* Set height to auto to accommodate the h1 tag */
	}

	.breadcrumb h1 {
		margin: 0; /* Remove default margins */
	}

	.calendar-button {
		display: inline-block;
		padding: 10px 20px;
		background-color: #30475e;
		color: #fff;
		text-decoration: none;
		border-radius: 5px;
	}
	.calendar-section {
		padding: 20px;
	}

	.content {
		padding: 20px;
	}

	@media screen and (max-width: 1200px) {
		/* Adjust the parallax height for larger screens */
		.parallax2 {
			height: 810px; /* Adjust the height as needed */
		}
	}

	@media screen and (max-width: 950px) {
		/* Adjust the parallax height for medium screens */
		.parallax2 {
			height: 750px; /* Adjust the height as needed */
		}
	}

	@media screen and (max-width: 600px) {
		/* Adjust the parallax height for smaller screens */
		.parallax2 {
			height: 720px; /* Adjust the height as needed */
		}
	}
</style>
