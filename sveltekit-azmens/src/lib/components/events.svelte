<div class="events-container">
	<div class="new-events">
		<a href="http://www.mensregion1champ.com/">
			<img src="/images/region1.jpg" alt="Slide 1" />
		</a>
		<div class="event-text">
			<p class="event-date">April 3 - 7</p>
			<p class="event-title">2024 Men's Region 1 ​Gymnastics Championships​</p>
			<p class="event-location">Mesa, Ariz.​</p>
		</div>
	</div>
	<div class="new-events">
		<a href="https://usagym.org/events/2024-mens-western-championships/">
			<img src="/images/westerns2.png" alt="Slide 2" />
		</a>
		<div class="event-text">
			<p class="event-date">April 26 - 28</p>
			<p class="event-title">2024 Men’s Western National Championships</p>
			<p class="event-location">Chandler, Ariz.</p>
		</div>
	</div>
	<div class="new-events">
		<a href="https://usagym.org/events/2024-mens-development-program-national-championships/">
			<img src="/images/nationals2.jpg" alt="Slide 3" />
		</a>
		<div class="event-text">
			<p class="event-date">May 9 - 12</p>
			<p class="event-title">2024 Men’s Development Program National Championships</p>
			<p class="event-location">Daytona Beach, Fla.</p>
		</div>
	</div>
</div>

<style>
	.event-text p {
		font-size: 1.5em;
		margin-bottom: 1em; /* Adjust this value as needed */
	}

	.event-location {
		color: #222831; /* Set the color of the location */
	}
	.event-title {
		font-size: 1.5em; /* Adjust this value as needed */
		color: #30475e;
		font-weight: bold; /* Add this line to increase the font weight */
	}

	.event-text {
		padding: 30px; /* Add padding as needed */
		border-top: 2px solid #ccc; /* Add a border to the top of the text */
	}

	.event-date {
		color: #f05454; /* Set the color of the date */
	}
	.events-container {
		display: flex;
		flex-wrap: wrap;
		justify-content: space-between;
	}

	.events-container .card img {
		width: 400px; /* Adjust this value as needed */
		height: 200px; /* Adjust this value as needed */
		object-fit: cover;
	}

	.new-events {
		width: 30%; /* Initially set to occupy 30% of the container width */
		margin: 20px 20px; /* Adjust this value as needed */
		box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2); /* Add shadow for card effect */
		border-radius: 5px; /* Rounded corners */
		background-color: #fff; /* Card background color */
		overflow: hidden; /* Ensures the image doesn't overflow the rounded corners */
	}

	.new-events img {
		width: 100%;
		height: auto;
		object-fit: cover;
		transition: transform 0.3s ease; /* Add this line for smooth hover effect */
	}

	.new-events img:hover {
		transform: scale(1.1); /* Add this line to scale the image on hover */
	}

	@media (min-width: 1200px) {
		.events-container {
			padding: 20px;
			max-width: 1200px; /* This will prevent the container (and therefore the cards) from spreading beyond 1200px */
			margin: 0 auto; /* Center the container */
		}

		.new-events {
			max-width: 400px; /* This will prevent the cards from growing beyond 400px */
			margin: 20px auto; /* Center-align and adjust margin */
		}
	}

	@media (min-width: 901px) and (max-width: 1199px) {
		.new-events {
			width: 45%;
		}

		.events-container {
			justify-content: center;
			padding: 40px;
		}
	}

	@media (max-width: 900px) {
		.events-container {
			justify-content: center;
			padding: 40px;
		}

		.new-events {
			width: 75%;
			margin: 20px auto;
		}

		.event-text p {
			font-size: 1.5em;
		}
	}

	@media (max-width: 600px) {
		.events-container {
			justify-content: center;
			padding: 40px;
		}

		.new-events {
			width: 90%;
			min-width: 300px; /* This will prevent the cards from shrinking beyond 300px */
			margin: 40px auto;
		}

		.event-text p {
			font-size: 1.5em;
		}
	}
</style>
