<script>
	import { goto } from '$app/navigation';
	let showLinks = false;

	function toggleLinks() {
		showLinks = !showLinks;
	}

	function navigateToHome() {
		goto('/');
	}

	function navigateToEvents() {
		goto('/events');
	}

	function navigateToCalendar() {
		goto('/calendar');
	}

	function navigateToImportantLinks() {
		goto('/important-links');
	}
</script>

<div class="toolbar" on:click={toggleLinks}>
	<div class="menu-icon">
		<div></div>
		<div></div>
		<div></div>
	</div>
	{#if showLinks}
		<nav class="navigation">
			<ul>
				<li><button type="button" on:click={navigateToHome}>Home</button></li>
				<li><button type="button" on:click={navigateToEvents}>Events</button></li>
				<li><button type="button" on:click={navigateToCalendar}>Calendar</button></li>
				<li><button type="button" on:click={navigateToImportantLinks}>Important Links</button></li>
			</ul>
		</nav>
	{/if}
</div>

<style>
	.toolbar {
		display: flex;
		justify-content: flex-end;
		align-items: center;
		padding: 10px;
		cursor: pointer;
		display: none; /* Hide the toolbar by default */
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

	.navigation {
		position: fixed; /* Make the navigation menu fixed */
		top: 105px; /* Position the navigation menu under the header */
		right: 0; /* Align the right edge with the right edge of the viewport */
		bottom: 150px; /* Align the bottom edge with the bottom edge of the viewport, leaving space for the footer */
		left: 0; /* Align the left edge with the left edge of the viewport */
		background-color: rgba(75, 39, 39, 0.8); /* Add opacity */
		display: flex; /* Make the navigation menu a flex container */
		justify-content: center; /* Center the content horizontally */
		align-items: center; /* Center the content vertically */
		padding-bottom: 50%; /* Add some bottom padding */
		transition: all 0.5s ease; /* Add a transition */
	}

	.navigation ul {
		list-style-type: none;
		margin: 0;
		padding: 0;
		display: flex; /* Make the list items display in a flex layout */
		flex-direction: column; /* Stack the list items vertically */
		align-items: center; /* Center the list items horizontally */
	}
	.navigation li button {
		display: block;
		background: #793434; /* Change the background color here */
		color: white;
		text-align: center;
		padding: 30px 60px; /* Increase left and right padding to make the buttons wider */
		font-size: 20px; /* Increase the font size */
		text-decoration: none;
		border: 2px solid rgb(89, 89, 89); /* Add a border */
		border-radius: 10px; /* Add rounded edges */
		cursor: pointer;
		margin: 0 auto 10px; /* Remove top margin to position the links right on top of each other */
	}

	.navigation li button:hover {
		background-color: rgb(89, 89, 89);
	}

	@media screen and (max-width: 900px) {
		.toolbar {
			display: block;
		}
	}
</style>
