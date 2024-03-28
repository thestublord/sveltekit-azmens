<div class="image">
	<img src="/images/2.png" alt="Slide 3" />
</div>

<style>
	.image {
		width: 100vw; /* 100% of the viewport width */
		height: auto; /* Automatically adjust height to maintain aspect ratio */
		max-height: 1000px; /* Maximum height of 1050px */
		overflow: hidden; /* Hide any overflow */
	}

	.image img {
		width: 100%; /* Full width */
		height: auto; /* Maintain aspect ratio */
		object-fit: cover; /* Cover the entire container while preserving aspect ratio */

		display: block; /* Needed for margin: auto to work */
	}

	@media (max-width: 900px) {
		.image img {
			transform: scale(1.3); /* Zoom in on the image */
		}
	}

	@media (min-width: 1200px) {
		.image img {
			margin-top: -80px; /* Move the image 100px higher */
		}
	}

	@media (min-width: 2000px) {
		.image img {
			margin-top: -285px; /* Move the image 100px higher */
		}
	}
</style>
