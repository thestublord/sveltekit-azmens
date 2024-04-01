<div class="events-container">
	<div class="new-events">
		<img src="/images/region1.jpg" alt="Slide 1" />
		<div class="event-text">
			<p class="event-date">April 3 - 7</p>
			<a href="http://www.mensregion1champ.com/" class="event-title">
				<p>2024 Men's Region 1 Championships​</p>
			</a>
			<p class="event-location">Mesa, Az.​</p>
		</div>
	</div>
	<div class="new-events">
		<img src="/images/westerns3.jpg" alt="Slide 2" />
		<div class="event-text">
			<p class="event-date">April 26 - 28</p>
			<a href="https://usagym.org/events/2024-mens-western-championships/" class="event-title">
				<p>2024 Men’s Western National Championships</p>
			</a>
			<p class="event-location">Chandler, Az.</p>
		</div>
	</div>
	<div class="new-events">
		<img src="/images/nationals2.jpg" alt="Slide 3" />
		<div class="event-text">
			<p class="event-date">May 9 - 12</p>
			<a
				href="https://usagym.org/events/2024-mens-development-program-national-championships/"
				class="event-title"
			>
				<p>2024 Men’s National Championships</p>
			</a>
			<p class="event-location">Daytona Beach, Fl.</p>
		</div>
	</div>
</div>

<style>
	.events-container {
		margin-top: 100px;
		display: flex;
		flex-wrap: wrap;
		justify-content: center; /* Center the card items horizontally */
		gap: 30px; /* Add some space between the card items */
		margin: 0 auto; /* Center the container itself */
		max-width: 1200px; /* Limit the width of the container */
		margin-bottom: 50px;
		font-family: 'Arial', sans-serif;
	}

	.new-events {
		margin-top: 60px;
		width: 23%; /* Make each card item take up approximately a quarter of the container's width */
		margin-bottom: 20px; /* Add some space below each card item */
		text-align: center; /* Center the text */
		color: #222831;
		border: 1px solid #ccc; /* Add a border */
		border-radius: 10px; /* Add rounded corners */
		box-shadow: 0 2px 5px rgba(0, 0, 0, 0.15); /* Add a box shadow */
		background-color: #dddddd;
	}

	.new-events img {
		width: 100%;
		height: auto;
		transition: none;
	}

	.event-text {
		background-color: #dddddd;
		padding: 10px;
		font-size: 1em; /* Set a base font size */
	}

	.event-date {
		font-weight: bold;
		font-size: 1.2em;
		color: #eb1b2d;
	}

	.event-title {
		font-size: 1.2em;
		color: #222831;
		transition: color 0.3s ease;
		text-decoration: none;
	}

	.event-title:hover {
		color: #007bff; /* Change the color when hovered over */
		text-decoration: underline; /* Add an underline when hovered over */
	}

	.event-location {
		font-style: italic;
		font-size: 1.2em;
		color: #30475e;
	}

	@media (max-width: 700px) {
		.events-container {
			gap: 0px; /* Reduce the space between the card items */
		}
		.new-events {
			width: 60%; /* Make each card item take up the full width of the card */
		}

		.event-text,
		.event-location {
			font-size: 1.2em; /* Reduce the font size */
		}

		.event-date {
			font-size: 1.2em; /* Reduce the font size */
		}

		.event-title {
			font-size: 1.5em; /* Reduce the font size */
		}
	}

	@media (max-width: 600px) {
		.event-text,
		.event-location {
			font-size: 1.1em; /* Further reduce the font size */
		}

		.event-date {
			font-size: 1.1em; /* Further reduce the font size */
		}

		.event-title {
			font-size: 1.4em; /* Further reduce the font size */
		}
	}

	@media (max-width: 1200px) {
		.event-title {
			font-size: 1.3em; /* Reduce the font size */
		}
	}
</style>
