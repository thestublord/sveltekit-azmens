<div class="pageHeader" style="background-color: #30475e;">
	<div class="pageHeaderTitle">About</div>
</div>

<div class="breadcrumb">
	<!-- Breadcrumb content goes here -->
</div>

<div class="container">
	<h1>AZMGA Committee</h1>
	<div class="card-container">
		<div class="card-item">
			<img src="/images/blank.png" alt="blank profile picture" />
			<h2>President</h2>
			<p>Clay Baimbridge</p>
		</div>
		<div class="card-item">
			<img src="/images/blank.png" alt="blank profile picture" />
			<h2>Vice President</h2>
			<p>Name</p>
		</div>
		<div class="card-item">
			<img src="/images/blank.png" alt="blank profile picture" />
			<h2>Treasurer</h2>
			<p>Name</p>
		</div>
		<div class="card-item">
			<img src="/images/blank.png" alt="blank profile picture" />
			<h2>Secretary</h2>
			<p>Name</p>
		</div>
	</div>

	<div class="container1">
		<div class="card1">
			<h1>Send us a message</h1>

			<h2>Email: example@example.com</h2>
		</div>
	</div>
</div>

<style>
	/* Add the following styles */

	.card1 h1 {
		font-size: 1.5em; /* Adjust as needed */
		color: #222831;
	}

	.card1 h2 {
		font-size: 1.2em; /* Adjust as needed */
		color: #30475e;
	}

	.container1 {
		display: flex;
		justify-content: center; /* Center horizontally */
		align-items: center; /* Center vertically */
		margin: 0 auto;
		max-width: 1200px;
		margin-top: 60px;
	}

	.card1 {
		padding: 20px;
		background-color: #dddddd;
		box-shadow: 0 2px 5px rgba(0, 0, 0, 0.15);
		border-radius: 10px;

		margin: 0 auto;
		color: #222831;
	}
	.container {
		margin: 0 auto; /* Center the container */
		margin-bottom: 50px;
		margin-top: 50px;
		font-family: 'Arial', sans-serif;
	}

	h2 {
		color: #222831; /* Set the color of the heading */
		font-size: 1.5em; /* Set the font size of the heading */
	}

	h1 {
		text-align: center; /* Center the heading */
		margin: 20px 0; /* Add some space above and below the heading */
		color: #222831;
		font-size: 2em; /* Set the font size of the heading */
	}

	.card-container {
		display: flex;
		flex-wrap: wrap;
		justify-content: center; /* Center the card items horizontally */
		gap: 20px; /* Add some space between the card items */
		margin: 0 auto; /* Center the container itself */
		max-width: 1200px; /* Limit the width of the container */
	}

	.card-item {
		width: 23%; /* Make each card item take up approximately a quarter of the container's width */
		margin-bottom: 20px; /* Add some space below each card item */
		text-align: center; /* Center the text */
		color: #000;

		border-radius: 10px; /* Add rounded corners */
		box-shadow: 0 2px 5px rgba(0, 0, 0, 0.15); /* Add a box shadow */
		background-color: #dddddd;
	}

	.card-item img {
		width: 100%; /* Make the image take up the full width of the card item */
		height: auto; /* Keep the original aspect ratio of the image */
	}

	.card-item h2 {
		margin-top: 20px; /* Add some space above the title */
	}

	.card-item p {
		margin-top: 10px; /* Add some space above the name */
		color: #30475e;
	}

	.breadcrumb {
		padding: 2px;
		background-color: #dddddd; /* Light grey background */
	}

	.pageHeader {
		padding: 90px 0;
	}

	.pageHeaderTitle {
		text-transform: uppercase;
		font-size: 2.7em; /* Responsive font size */

		color: #fff;
		text-align: center;
	}

	@media (max-width: 400px) {
		.card1 {
			max-width: 80%; /* Set a maximum width for the card */
		}
	}

	@media (max-width: 600px) {
		.card-item {
			width: 60%; /* Make each card item take up the full width of the card */
		}
	}

	@media screen and (max-width: 600px) {
		.pageHeaderTitle {
			font-size: 2em; /* Reduced font size for smaller screens */
		}

		h1 {
			font-size: 1.8em; /* Set the font size of the heading */
		}
	}
</style>
