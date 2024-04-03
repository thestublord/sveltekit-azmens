<script>
	import { onMount } from 'svelte';

	onMount(() => {
		// Set a CSS variable for the height
		document.documentElement.style.setProperty('--vh', `${window.innerHeight * 0.01}px`);

		// Listen for the resize event and update the height
		window.addEventListener('resize', () => {
			document.documentElement.style.setProperty('--vh', `${window.innerHeight * 0.01}px`);
		});
	});
</script>

<div class="videocontainer">
	<video muted autoplay playsinline loop>
		<source src="u.mp4" type="video/mp4" />
		<track kind="captions" src="captions.vtt" srclang="en" label="English" />
		Your browser does not support the video tag.
	</video>
</div>

<style>
	/* Adjust the video container and video styles for responsiveness */
	.videocontainer {
		position: relative;
		width: 100%;
		height: calc(var(--vh, 1vh) * 70); /* Use the CSS variable for the height */
		overflow: hidden;
	}

	video {
		width: 100%; /* Take up the full width of its parent */
		height: 100%; /* Take up the full height of its parent */
		object-fit: cover; /* Cover the entire area of the container */
		min-width: 300px;
	}

	@media screen and (max-width: 600px) {
		/* Adjust the video container height for smaller screens */
		video {
			transform: scale(1.9); /* Zoom in on the video */
		}
		.videocontainer {
			height: 35vh; /* Adjust the height as needed */
		}
	}

	@media screen and (min-width: 600px) {
		/* Adjust the video container height for smaller screens */
		video {
			transform: scale(1.9); /* Zoom in on the video */
		}
		.videocontainer {
			height: 45vh; /* Adjust the height as needed */
		}
	}

	@media screen and (min-width: 768px) {
		/* Adjust the video container height for medium screens */
		.videocontainer {
			height: 55vh; /* Adjust the height as needed */
		}
	}

	@media screen and (min-width: 992px) {
		/* Adjust the video container height for medium screens */
		.videocontainer {
			height: 45vh; /* Adjust the height as needed */
		}

		video {
			transform: scale(1.4); /* Zoom in on the video */
		}
	}

	@media screen and (min-width: 1200px) {
		/* Adjust the video container height for larger screens */

		video {
			width: 80%; /* Shrink the video width */
			height: 90%; /* Shrink the video height */
			object-position: center; /* Center the video */
		}

		.videocontainer {
			height: 40vh; /* Adjust the height as needed */
		}
	}

	@media screen and (min-width: 2500px) {
		/* Adjust the video container height for larger screens */

		video {
			width: 75%; /* Shrink the video width */
			height: 85%; /* Shrink the video height */
			object-position: center; /* Center the video */
		}

		.videocontainer {
			height: 40vh; /* Adjust the height as needed */
		}
	}
</style>
