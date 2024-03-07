<script>
	import Toolbar from './toolbar.svelte';
	import { goto } from '$app/navigation';

	function navigateToHome(event) {
		if (event.type === 'click' || (event.type === 'keydown' && event.key === 'Enter')) {
			goto('/');
		}
	}

	function navigateToEvents(event) {
		if (event.type === 'click' || (event.type === 'keydown' && event.key === 'Enter')) {
			goto('/events');
		}
	}

	function navigateToCalendar(event) {
		if (event.type === 'click' || (event.type === 'keydown' && event.key === 'Enter')) {
			goto('/calendar');
		}
	}

	function navigateToImportantLinks(event) {
		if (event.type === 'click' || (event.type === 'keydown' && event.key === 'Enter')) {
			goto('/important-links');
		}
	}
</script>

<header>
	<div class="header-content">
		<!-- Wrap the image, text, and navigation inside a container -->

		<div class="logo-container">
			<!-- Wrap the image inside an anchor tag -->
			<a href="/" aria-label="Navigate to Home">
				<img
					src="/images/abc073496eab0773f7be106681d7613d.jpeg"
					alt="Arizona Men's Gymnastics Association Logo"
					class="left-image"
				/>
			</a>
			<!-- Position the text under the image -->
			<div class="header-text">
				<h1>AMGA</h1>
			</div>
		</div>

		<nav class="navigation-header">
			<div class="nav-button-header">
				<ul>
					<li>
						<button type="button" on:click={navigateToHome} on:keydown={navigateToHome}>Home</button
						>
					</li>
					<li>
						<button type="button" on:click={navigateToEvents} on:keydown={navigateToEvents}
							>Events</button
						>
					</li>
					<li>
						<button type="button" on:click={navigateToCalendar} on:keydown={navigateToCalendar}
							>Calendar</button
						>
					</li>
					<li>
						<button
							type="button"
							on:click={navigateToImportantLinks}
							on:keydown={navigateToImportantLinks}>Important Links</button
						>
					</li>
					<!-- Add more navigation links as needed -->
				</ul>
			</div>
		</nav>

		<Toolbar />
	</div>
</header>

<nav class="navigation">
	<ul>
		<li>
			<button type="button" on:click={navigateToHome} on:keydown={navigateToHome}>Home</button>
		</li>
		<li>
			<button type="button" on:click={navigateToEvents} on:keydown={navigateToEvents}>Events</button
			>
		</li>
		<li>
			<button type="button" on:click={navigateToCalendar} on:keydown={navigateToCalendar}
				>Calendar</button
			>
		</li>
		<li>
			<button
				type="button"
				on:click={navigateToImportantLinks}
				on:keydown={navigateToImportantLinks}>Important Links</button
			>
		</li>
		<!-- Add more navigation links as needed -->
	</ul>
</nav>

<main class="main-content">
	<!-- Main content here -->
</main>

<style>
	header {
		background-position: fixed; /* Add fixed background position */
		color: white;
		padding: 2rem; /* Add padding to the header */
	}
	.header-content {
		display: flex;
		align-items: center;
		justify-content: space-between;
		font-size: 8px; /* Adjust font size of the header */
		text-align: center;
		height: 60px; /* Fixed height */
		overflow: hidden; /* Prevent content from overflowing */
		background-position: fixed; /* Add fixed background position */
	}

	.logo-container {
		display: flex;
		flex-direction: row; /* Arrange items vertically */
		align-items: center; /* Center items horizontally */
		justify-content: space-between; /* Space items evenly */
	}

	.navigation {
		background-color: #793434;
		padding: 10px;
		margin-bottom: 10px;
		height: 18px;
		align-items: center;
	}

	.navigation-header {
		display: none;
	}

	nav ul {
		list-style-type: none;
		padding: 0;
		margin: 0;
		display: flex;
		justify-content: space-around;
		gap: 1rem;
	}

	nav li {
		margin: 0 1rem;
	}

	nav button {
		background: none;
		border: none;
		color: white;
		font-size: 18px;
		cursor: pointer;
		text-decoration: none;
		padding: 0;
	}

	nav button:hover {
		text-decoration: underline;
	}

	.left-image {
		width: 80px; /* Adjust size as needed */
		height: auto; /* Maintain aspect ratio */
		margin-top: 10px; /* Adjust top margin to create space */
		margin-bottom: 10px; /* Adjust bottom margin to create space */
		margin-right: 20px; /* Align the left image to the left */
		margin-left: 0; /* Align the left image to the left */
	}

	.header-text {
		text-align: center;
		width: 100%;
	}

	@media screen and (min-width: 500px) {
		header {
			background: linear-gradient(45deg, rgb(89, 89, 89) 30%, #793434 0);

			color: white;
			padding: 1rem; /* Add padding to the header */
			height: 60px; /* Fixed height */
		}
	}

	nav ul {
		display: flex; /* Keep navigation links horizontally aligned */
		justify-content: center; /* Center navigation links */
		gap: 1rem; /* Adjust spacing between navigation links */
	}

	nav li {
		margin: 0 1rem; /* Add margin around navigation links */
	}

	@media screen and (min-width: 800px) {
		header {
			background: linear-gradient(45deg, rgb(89, 89, 89) 400%, #793434 0);

			color: white;
			padding: 1rem; /* Add padding to the header */
			height: 60px; /* Fixed height */
		}
	}

	/* Adjustments for mobile devices */
	@media only screen and (max-width: 900px) {
		.navigation {
			display: none; /* Hide the navigation links */
		}

		nav ul {
			display: flex; /* Keep navigation links horizontally aligned */
			justify-content: flex-start; /* Align navigation links to the start (left) */
			gap: 0.2rem; /* Adjust spacing between navigation links */
		}

		nav li {
			margin: 0 0.2rem; /* Add margin around navigation links */
		}

		.left-image {
			margin: 0 auto; /* Center the left image for smaller screens */
		}

		.header-text {
			text-align: center; /* Center header text for smaller screens */
			margin-left: 20px;
		}

		.header-text h1 {
			font-size: 16px; /* Reduce font size of header text for smaller screens */
		}

		header {
			background: linear-gradient(45deg, rgb(89, 89, 89) 50%, #793434 0);
			background-position: fixed; /* Add fixed background position */
			color: white;
			padding: 1rem; /* Add padding to the header */
			height: 60px; /* Fixed height */
		}
	}

	/* Add more media queries as needed */

	/* Show navigation-header and hide .navigation at 2000px */
	@media screen and (min-width: 1250px) {
		.navigation-header {
			display: block; /* Show navigation-header */
			font-size: 40px; /* Adjust font size of the navigation links */
		}

		.navigation {
			display: none; /* Hide .navigation */
		}

		header {
			background: linear-gradient(45deg, rgb(89, 89, 89) 50%, #793434 0);
			background-position: fixed; /* Add fixed background position */
			color: white;
			padding: 1rem; /* Add padding to the header */
			height: 60px; /* Fixed height */
		}
	}
</style>
