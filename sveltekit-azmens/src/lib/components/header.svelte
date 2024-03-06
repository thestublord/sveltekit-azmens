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
		<div class="logo-and-navigation-container">
			<!-- Wrap the image and text inside a container -->
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
			<div class="nav-text">
				<nav class="navigation-header">
					<ul>
						<li>
							<button type="button" on:click={navigateToHome} on:keydown={navigateToHome}
								>Home</button
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
				</nav>
			</div>
		</div>
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
		background-color: #793434;
		color: white;
		padding: 1rem;
	}

	.header-content {
		display: flex;
		align-items: center;
		justify-content: space-between;
		font-size: 8px; /* Adjust font size of the header */
		text-align: center;
	}

	.logo-container {
		display: flex;
		flex-direction: column; /* Arrange items vertically */
		align-items: center; /* Center items horizontally */
	}

	.navigation {
		background-color: #ccc;
		padding: 10px;
		margin-bottom: 20px;
	}

	.navigation-header {
		display: none;
	}

	.navigation-header ul {
		list-style-type: none;
		padding: 0;
		margin: 0;
		display: flex;
		justify-content: space-around;
		gap: 1rem;
		font-size: 30px;
		margin-left: auto; /* Push the links to the right */
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
		color: rgb(16, 12, 12);
		font-size: 18px;
		cursor: pointer;
		text-decoration: none;
		padding: 0;
	}

	nav button:hover {
		text-decoration: underline;
	}

	.left-image {
		width: 100px; /* Adjust size as needed */
		height: auto; /* Maintain aspect ratio */
		margin-top: 10px; /* Adjust top margin to create space */
		margin-bottom: 10px; /* Adjust bottom margin to create space */
		margin-right: auto; /* Align the left image to the left */
		margin-left: 0; /* Align the left image to the left */
	}

	.header-text {
		text-align: center;
		width: 100%;
	}

	.toolbar {
		display: flex;
		align-items: center;
		cursor: pointer;
		margin-left: auto; /* Align the toolbar to the right */
	}

	.menu-icon {
		width: 30px;
		height: 20px;
		display: flex;
		flex-direction: column;
		justify-content: space-between;
	}

	.menu-icon div {
		width: 100%;
		height: 4px;
		background-color: #ccc;
	}

	/* Adjustments for mobile devices */
	@media only screen and (max-width: 900px) {
		header {
			padding: 1rem; /* Reduce header padding for smaller screens */
		}

		.navigation {
			display: none; /* Hide the navigation links */
		}

		nav ul {
			display: flex; /* Keep navigation links horizontally aligned */
			justify-content: center; /* Center navigation links horizontally */
			gap: 1rem; /* Adjust spacing between navigation links */
		}

		nav li {
			margin: 0 1rem; /* Add margin around navigation links */
		}

		.left-image {
			margin: 0 auto; /* Center the left image for smaller screens */
		}

		.header-text {
			text-align: center; /* Center header text for smaller screens */
		}

		.header-text h1 {
			font-size: 20px; /* Reduce font size of header text for smaller screens */
		}
	}

	/* Adjustments for full-screen mode */
	@media screen and (min-width: 1024px) {
		header {
			padding: 1rem; /* Reduce header padding for full-screen mode */
		}
	}

	/* Add more media queries as needed */

	/* Show navigation-header and hide .navigation at 2000px */
	@media screen and (min-width: 1250px) {
		.logo-and-navigation-container {
			display: flex;
			justify-content: space-between;
			align-items: center; /* Align items vertically in the center */
		}

		.navigation-header {
			display: block; /* Show navigation-header */
			font-size: 40px; /* Adjust font size of the navigation links */
		}

		.navigation {
			display: none; /* Hide .navigation */
		}
	}
</style>
