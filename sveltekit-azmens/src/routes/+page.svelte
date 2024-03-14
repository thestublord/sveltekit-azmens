<script>
	import Events from '../lib/components/events.svelte';
	import Video from '../lib/components/video.svelte';
</script>

<Video class="video-section" />

<div class="content">
	<Events />
</div>

<style>
	.video-section {
		position: fixed;
		top: 0;
		left: 0;
		width: 100%;
		height: 100vh;
		object-fit: cover;
		z-index: -1;
	}

	@media (min-width: 1250px) {
		.video-section {
			max-width: 1250px;
		}
	}
</style>
