<main class="main-content">
	<div class="large-box">
		<div class="small-box"></div>
		<div class="small-box"></div>
	</div>
	<!-- Add other main content here -->
</main>

<style>
	/* Other CSS styles remain unchanged */

	/* Style for the large box */
	.large-box {
		background-color: #793535;
		width: 80%; /* Set the width to cover most of the page */
		height: 70%; /* Set the height to cover most of the page */
		margin: 0 auto; /* Center the box horizontally */
		padding: 25px; /* Add padding for better appearance */
		position: absolute;
		top: 20%; /* Position the box below the nav and header */
		left: 50%;
		transform: translateX(-50%);
		display: flex; /* Use flexbox to arrange the small boxes */
		justify-content: space-between; /* Space the small boxes evenly */
	}

	/* Style for the small boxes */
	.small-box {
		background-color: #4d4949; /* Example background color for small boxes */
		width: 48%; /* Set the width of the small boxes */
		height: 100%; /* Set the height of the small boxes to fill the large box */
	}

	/* Adjust large box and small box styles for smaller screens */
	@media screen and (max-width: 768px) {
		.large-box {
			width: 90%; /* Adjust width for smaller screens */
			height: auto; /* Allow the height to adjust based on content */
			flex-direction: column; /* Stack the small boxes vertically */
			align-items: center; /* Center the small boxes horizontally */
			top: 50%; /* Adjust top position for smaller screens */
			transform: translateY(-50%) translateX(-50%);
		}

		.small-box {
			width: 100%; /* Set the width of the small boxes to 100% for smaller screens */
			margin-bottom: 20px; /* Add margin between the small boxes */
		}
	}
</style>
