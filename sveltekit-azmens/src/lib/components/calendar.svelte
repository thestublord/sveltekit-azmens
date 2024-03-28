<div class="wrapper">
	<div class="iframe-container">
		<iframe
			src="https://calendar.google.com/calendar/embed?src=azmgabackend%40gmail.com&ctz=America%2FPhoenix"
			style="border: 0"
			width="100%"
			height="100%"
			frameborder="0"
			scrolling="no"
		></iframe>
	</div>
</div>

<style>
	.wrapper {
		/* Removed height: 100vh; */
		padding: 30px; /* Add space around the wrapper */
		max-width: 1200px; /* Maximum width */
		margin: auto; /* Center the container */
	}
	.iframe-container {
		padding-top: 100px;
		position: relative;
		padding-bottom: 56.25%; /* 16:9 Aspect Ratio */
		overflow: hidden;
		max-width: 100%;
		margin-bottom: 50px; /* Add a bottom margin */
	}

	.iframe-container iframe {
		position: absolute;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
	}

	@media (max-width: 600px) {
		.iframe-container {
			padding-bottom: 75%; /* Adjust to desired aspect ratio for small screens */
		}
	}

	@media (min-width: 601px) and (max-width: 1199px) {
		.iframe-container {
			padding-bottom: 60%; /* Adjust to desired aspect ratio for medium screens */
		}
	}

	@media (min-width: 1200px) {
		.iframe-container {
			padding-bottom: 50%; /* Adjust to desired aspect ratio for large screens */
		}
	}
</style>
