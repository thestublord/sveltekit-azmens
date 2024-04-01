<script>
	import { goto } from '$app/navigation';
	import Events from '../lib/components/events.svelte';
	import Video from '../lib/components/video.svelte';
</script>

<div class="wrapper">
	<div class="video">
		<Video />
	</div>

	<div class="breadcrumb">
		<h1>Upcoming Events</h1>
	</div>

	<div class="breadcrumb2">
		<!-- Breadcrumb content goes here -->
	</div>

	<div class="events-section"></div>
	<div class="content">
		<Events />
	</div>

	<div class="breadcrumb1">
		<!-- Breadcrumb content goes here -->
	</div>

	<div class="parallax2">
		<div class="button-container">
			<button on:click={() => goto('/calendar')} class="calendar-button">Go to Calendar</button>
			<button on:click={() => goto('/contact')} class="calendar-button">Contact</button>
			<button on:click={() => goto('/about')} class="calendar-button">About</button>
		</div>
	</div>
</div>

<style>
	/* Adjustments to the styles */

	.breadcrumb2 {
		padding: 2px;
		background-color: #f05454; /* Light grey background */
	}

	h1 {
		font-size: 2em; /* Default font size */
	}

	.wrapper {
		display: flex;
		flex-direction: column;
		width: 100%;
		font-family: 'Arial', sans-serif;
	}
	.breadcrumb1 {
		padding: 2px;
		background-color: #222831; /* Light grey background */
	}

	.parallax2 {
		background-image: url('/images/3.png');
		height: 600px;
		background-attachment: fixed;
		background-position: center;
		background-repeat: no-repeat;
		background-size: cover;
	}

	.breadcrumb {
		padding: 10px;
		background-color: #30475e;
		height: auto; /* Set height to auto to accommodate the h1 tag */
	}

	.breadcrumb h1 {
		margin: 0; /* Remove default margins */
	}

	.content {
		padding: 20px;
		display: flex;
		flex-direction: column;
		align-items: center; /* Center children vertically */
		justify-content: space-between; /* Distribute space evenly between children */
	}

	.button-container {
		display: flex;
		flex-direction: column;
		align-items: center; /* Center the buttons horizontally */
		justify-content: center; /* Center the buttons vertically */
		margin-top: 80px; /* Add a top margin to move the buttons lower */
		gap: 20px; /* Add space between the buttons */
		font-family: 'Arial', sans-serif;
	}

	.calendar-button {
		display: inline-block;
		background-color: #30475e; /* Add the background color */
		color: white; /* Add the text color */
		border: 2px solid #222831; /* Add a 2px white border */
		border-radius: 10px; /* Add roundness to the buttons */
		opacity: 1; /* Keep the opacity as 1 */
		transition: background-color 0.3s ease; /* Add transition for smooth hover effect */
		text-decoration: none;
		border-radius: 5px;
		padding: 20px 30px; /* Increase padding to make the button bigger */
		font-size: 1.2em; /* Increase font size to make the text bigger */
		justify-content: center; /* Center the buttons */
		margin: 10px 0; /* Add some margin to the top and bottom */
		width: 350px; /* Increase width to make the button bigger */
		height: 80px;
	}

	.calendar-button:hover {
		background-color: #dddddd; /* Change the background color on hover */
		color: #222831; /* Change the text color on hover */
	}

	@media screen and (max-width: 1200px) {
		/* Adjust the parallax height for larger screens */

		h1 {
			font-size: 2.2em; /* Smaller font size for larger screens */
		}
	}

	@media screen and (max-width: 950px) {
		/* Adjust the parallax height for medium screens */

		h1 {
			font-size: 1.75em; /* Smaller font size for medium screens */
		}

		.calendar-button {
			width: 250px; /* Set maximum width at 1200px breakpoint */
			font-size: 1em; /* Decrease font size */
		}
	}

	@media screen and (max-width: 600px) {
		/* Adjust the parallax height for smaller screens */

		.calendar-button {
			width: 200px; /* Decrease width */
			height: 60px; /* Decrease height */
			padding: 10px 15px; /* Decrease padding */
			font-size: 1em; /* Decrease font size */
		}
	}
</style>
