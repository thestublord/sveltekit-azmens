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
				<li><button type="button" on:click={navigateToImportantLinks}>More</button></li>
			</ul>
		</nav>
	{/if}
</div>

<style>
	.toolbar {
		display: flex;
		justify-content: flex-end;
		align-items: center;
		padding: 17px;
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
		height: 10%;
		background-color: #f05454;
	}

	.navigation-toolbar {
		position: absolute; /* Add this line */
		top: 100%; /* Adjust this value as needed */
		right: 0;
		background: #30475e;
		width: 100%;
		text-align: center;
		border: 1px solid #f05454;
		box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.2);
		/* Add padding to the top and bottom */
		padding: 10px 0;
	}

	.navigation-toolbar li button {
		color: #fff; /* Change the text color to white for better contrast */
	}

	.navigation li button:hover {
		background-color: #2614bf;
	}
	.menu-icon div:hover {
		background-color: #f05454;
	}

	@media screen and (max-width: 900px) {
		.toolbar {
			display: block;
		}
	}
</style>
