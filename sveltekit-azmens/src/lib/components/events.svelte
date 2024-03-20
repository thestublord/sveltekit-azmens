<div class="events-container">
	<div class="new-events">
		<a href="http://www.mensregion1champ.com/">
			<img src="/images/14k.png" alt="Slide 1" />
		</a>
	</div>
	<div class="new-events">
		<a href="https://usagym.org/events/2024-mens-western-championships/">
			<img src="/images/westerns.png" alt="Slide 2" />
		</a>
	</div>
	<div class="new-events">
		<a href="https://usagym.org/events/2024-mens-development-program-national-championships/">
			<img src="/images/nationals.png" alt="Slide 3" />
		</a>
	</div>
</div>

<style>
	.events-container {
		display: flex;
		justify-content: space-around;
		align-items: center;
		flex-wrap: wrap;
	}

	.new-events {
		width: 30%;
		margin: 20px 20px; /* Adjust this value as needed */
	}

	.new-events img {
		width: 100%;
		height: auto;
		object-fit: cover;
		transition: transform 0.3s ease; /* Add this line */
	}

	.new-events img:hover {
		transform: scale(1.1); /* Add this line */
	}

	@media (max-width: 900px) {
		.new-events {
			width: 60%;
			margin: 40px auto; /* Adjust this value as needed */
		}
	}
</style>
