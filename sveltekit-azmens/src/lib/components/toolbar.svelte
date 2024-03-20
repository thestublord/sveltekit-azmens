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
		<nav class="navigation-toolbar">
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
		padding: 40px;
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
		background-color: #fdfdfd;
	}

	.navigation-toolbar {
		position: absolute; /* Add this line */
		top: 70px; /* Adjust this value as needed */
		right: 0;
		background: #146a83;
		width: 100%;
		text-align: center;
	}

	.navigation li button {
		display: block;
		background: #793434; /* Change the background color here */
		color: #fe545d;
		text-align: center;
		padding: 30px 60px; /* Increase left and right padding to make the buttons wider */
		font-size: 20px; /* Increase the font size */
		text-decoration: none;
		border: 2px solid #f75001; /* Add a border */
		border-radius: 10px; /* Add rounded edges */
		cursor: pointer;
		margin: 0 auto 10px; /* Remove top margin to position the links right on top of each other */
	}

	.navigation li button:hover {
		background-color: #fe545d;
	}
	.menu-icon div:hover {
		background-color: #fe545d;
	}

	@media screen and (max-width: 900px) {
		.toolbar {
			display: block;
		}
	}
</style>
