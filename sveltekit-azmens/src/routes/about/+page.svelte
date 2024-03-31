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
			<img src="/images/blank.png" alt="Description of the image" />
			<h2>President</h2>
			<p>Clay Baimbridge</p>
		</div>
		<div class="card-item">
			<img src="/images/blank.png" alt="Description of the image" />
			<h2>Vice President</h2>
			<p>Name</p>
		</div>
		<div class="card-item">
			<img src="/images/blank.png" alt="Description of the image" />
			<h2>Treasurer</h2>
			<p>Name</p>
		</div>
		<div class="card-item">
			<img src="/images/blank.png" alt="Description of the image" />
			<h2>Secretary</h2>
			<p>Name</p>
		</div>
	</div>

	<h1>Our Mission</h1>
	<div class="card">
		<p>
			Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam nec purus nec nunc tincidunt
			tincidunt. Nullam quis mauris nec nunc tincidunt tincidunt. Nullam quis mauris nec nunc
			tincidunt tincidunt. Nullam quis mauris nec nunc tincidunt tincidunt. Nullam quis mauris nec
			nunc tincidunt tincidunt. Nullam quis mauris nec nunc tincidunt tincidunt. Nullam quis mauris
			nec nunc tincidunt tincidunt. Nullam quis mauris nec nunc tincidunt tincidunt. Nullam quis
			mauris nec nunc tincidunt tincidunt. Nullam quis mauris nec nunc tincidunt tincidunt. Nullam
			quis mauris nec nunc tincidunt tincidunt. Nullam quis mauris nec nunc tincidunt tincidunt.
			Nullam quis mauris nec nunc tincidunt
		</p>
	</div>
</div>

<style>
	/* Add the following styles */

	h2 {
		color: #f05454; /* Set the color of the heading */
	}

	h1 {
		text-align: center; /* Center the heading */
		margin: 20px 0; /* Add some space above and below the heading */
		color: #222831;
	}

	.card {
		padding: 20px;

		border-radius: 10px; /* Rounded corners */

		/* Other properties */
		display: flex; /* Arrange the card items in a row */
		flex-wrap: wrap; /* Allow the card items to wrap onto multiple lines */
		justify-content: space-between; /* Add space between the card items */
		color: #000;
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
		border: 1px solid #ccc; /* Add a border */
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
	}

	.breadcrumb {
		padding: 2px;
		background-color: #f05454; /* Light grey background */
	}

	.pageHeader {
		padding: 100px 0;
	}

	.pageHeaderTitle {
		text-transform: uppercase;
		font-size: 4vw; /* Responsive font size */
		line-height: 1.1; /* Adjust line height */
		color: #fff;
		text-align: center;
	}

	@media screen and (max-width: 600px) {
		.pageHeaderTitle {
			font-size: 6vw; /* Increase font size on small screens */
		}
	}

	@media screen and (min-width: 601px) and (max-width: 1200px) {
		.pageHeaderTitle {
			font-size: 5vw; /* Decrease font size on medium screens */
		}
	}

	@media screen and (min-width: 1201px) {
		.pageHeaderTitle {
			font-size: 3vw; /* Decrease font size on large screens */
		}
	}

	@media (max-width: 600px) {
		.card-item {
			width: 70%; /* Make each card item take up the full width of the card */
		}
	}
</style>
