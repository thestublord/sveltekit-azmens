<script>
	import Events from '../lib/components/events.svelte';
	import Video from '../lib/components/video.svelte';
	import Calendar from '../lib/components/calendar.svelte';
	import Footer from '../lib/components/footer.svelte';
</script>

<div class="video-section">
	<Video />
</div>

<div class="events-section">
	<div class="bar"></div>
	<h1>Upcoming Events</h1>
	<div class="bar"></div>
	<div class="content">
		<Events />
	</div>
</div>

<div class="calendar-section">
	<div class="bar"></div>
	<h1>Calendar</h1>
	<div class="bar"></div>
	<div class="content">
		<Calendar />
	</div>
</div>

<Footer />

<style>
	/* Adjustments to the styles */

	.bar {
		height: 2px;
		background-color: #000;
		margin: 5px 0;
	}

	.video-section,
	.events-section,
	.calendar-section {
		padding: 20px 0;
	}

	.content {
		padding: 20px;
		background-color: #fdfdfd;
	}
</style>
