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
					src="/images/arizona-flag-large.jpg"
					alt="Arizona Men's Gymnastics Association Logo"
					class="left-image"
				/>
			</a>
			<!-- Position the text under the image -->
			<div class="header-text">
				<h1>Arizona<br />Men's<br />Gymnastics<br />Association</h1>
			</div>
		</div>

		<nav class="navigation-header">
			<ul>
				<li>
					<button type="button" on:click={navigateToHome} on:keydown={navigateToHome}>Home</button>
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
		</nav>

		<Toolbar />
	</div>
</header>

<main class="main-content">
	<!-- Main content here -->
</main>

<style>
	header {
		position: fixed; /* Position the header */
		top: 0; /* Align the header to the top */
		left: 0; /* Align the header to the left */
		right: 0; /* Align the header to the right */
		background: linear-gradient(45deg, #146a83 35%, #002645 0);
		color: #fff8e0;
		padding: 1rem; /* Add padding to the header */
		height: 60px; /* Fixed height */
		display: flex; /* Ensure content alignment */
		align-items: center; /* Align content vertically */
		justify-content: space-between; /* Align content horizontally */
		z-index: 1000; /* Ensure it's on top of everything else */
	}

	.header-content {
		display: flex;
		align-items: center;
		justify-content: space-between;
		font-size: 8px;
		text-align: center;
		width: 100%;
	}

	.logo-container {
		display: flex;
		flex-direction: row; /* Arrange items vertically */
		align-items: center; /* Center items horizontally */
		justify-content: space-between; /* Space items evenly */
	}

	.navigation-header {
		z-index: 1; /* Make sure the navigation header is above other elements */
		display: none; /* Hide navigation-header by default */
	}

	nav ul {
		list-style-type: none;
		padding: 0;
		margin: 0;
		display: flex;
		justify-content: space-around;
	}

	nav li {
		margin: 0 1rem;
	}

	nav button {
		background: none;
		border: none;
		color: #fff8e0;
		font-size: 18px;
		cursor: pointer;
		text-decoration: none;
		padding: 0;
	}

	nav button:hover {
		color: #f75001;
	}

	.left-image {
		width: 100px; /* Adjust size as needed */
		height: auto; /* Maintain aspect ratio */
		margin-right: 20px; /* Align the left image to the left */
	}

	.header-text {
		text-align: center;
		width: 100%;
	}

	@media screen and (min-width: 901px) {
		.navigation-header {
			display: block; /* Show navigation-header */
		}
	}

	@media screen and (max-width: 900px) {
		.header-text {
			display: none; /* Hide the header text */
		}
	}

	@media screen and (min-width: 900px) {
		.navigation-header {
			text-align: center; /* Center alignment after 900px */
		}

		@media screen and (min-width: 1251px) {
			/* Remove the duplicate z-index declaration */
		}

		nav ul {
			justify-content: center; /* Center the navigation links */
		}

		nav li {
			margin: 0 2rem; /* Increase the margin */
		}
	}
</style>
