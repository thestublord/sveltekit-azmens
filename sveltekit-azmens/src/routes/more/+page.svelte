<div>
	<div class="card">
		<div class="card-content">
			<img class="card-image" src="/images/region1.jpg" alt="Slide 1" />
			<div class="event-text">
				<p class="event-date">April 26 - 28</p>
				<a href="https://usagym.org/events/2024-mens-western-championships/" class="event-title">
					<p>2024 Men’s Western National Championships</p>
				</a>
				<p class="event-location">Chandler, Az.</p>
			</div>
		</div>
	</div>
</div>

<style>
	.card {
		border: 1px solid #ccc;
		border-radius: 5px;
		margin: 10px;
		padding: 10px;
		background-color: beige;
	}

	.card-content {
		display: flex; /* Use Flexbox */
		align-items: center; /* Center vertically */
	}

	.card-image {
		max-width: 30%; /* Adjust as needed */
		height: auto;
		margin-right: 0px; /* Space between the image and the text */
	}

	.event-date {
		font-weight: bold;
	}

	/* When the screen is 600px or less, stack the image and text vertically */
	@media (max-width: 600px) {
		.card-content {
			flex-direction: column;
		}

		.card-image {
			max-width: 100%;
			margin-bottom: 10px; /* Space below the image */
		}
	}
</style>
