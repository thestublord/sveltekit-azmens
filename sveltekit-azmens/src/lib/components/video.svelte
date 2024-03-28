<div class="videocontainer">
	<video muted autoplay playsinline loop>
		<source src="Designhhjkjh.mp4" type="video/mp4" />
		<track kind="captions" src="captions.vtt" srclang="en" label="English" />
		Your browser does not support the video tag.
	</video>
</div>

<style>
	/* Adjust the video container and video styles for responsiveness */
	.videocontainer {
		position: relative; /* Position the video container */
		width: 100%; /* Full width */
		height: 100vh; /* Full viewport height */
		overflow: hidden; /* Hide anything that exceeds the container */
	}

	video {
		width: 100%; /* Take up the full width of its parent */
		height: 100%; /* Take up the full height of its parent */
		object-fit: cover; /* Cover the entire area of the container */
	}

	@media screen and (max-width: 1200px) {
		/* Adjust the video container height for larger screens */
		.videocontainer {
			height: 65vh; /* Adjust the height as needed */
		}
	}

	@media screen and (max-width: 900px) {
		/* Adjust the video container height for medium screens */
		.videocontainer {
			height: 65vh; /* Adjust the height as needed */
		}
	}

	@media screen and (max-width: 600px) {
		/* Adjust the video container height for smaller screens */
		.videocontainer {
			height: 50vh; /* Adjust the height as needed */
		}
	}
</style>
