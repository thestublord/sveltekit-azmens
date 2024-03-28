<div class="wrapper">
	<div class="image">
		<img src="/images/3.png" alt="Slide 3" />
	</div>
</div>

<style>
	.wrapper {
		position: relative;
		width: 100%;
		height: 100vh;
		overflow: hidden;
	}

	.image {
		position: relative;
		width: 100%;
		height: 100%;
	}

	.image img {
		width: 100%; /* Take up the full width of its parent */
		height: auto; /* Scale height while maintaining aspect ratio */
		object-fit: cover; /* Cover the entire area of the container */
	}

	@media screen and (max-width: 900px) {
		.wrapper {
			height: auto; /* Adjust the height based on the content */
		}
	}
</style>
