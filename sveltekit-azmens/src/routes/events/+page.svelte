<script>
	import Carousel from '../../lib/components/carousel.svelte';
	import Events from '../../lib/components/events.svelte';
</script>

<div class="events-section">
	<h1>Upcoming Events</h1>
	<div class="bar"></div>
</div>

<Carousel />
<Events />

<style>
	/* Add the following styles */

	.bar {
		height: 2px; /* Height of the bar */
		background-color: #000; /* Color of the bar */
		margin: 50px 0 50px 0; /* Add top margin */
	}

	.events-section {
		background-color: #fe9769; /* Change color of the events section */
	}
</style>
