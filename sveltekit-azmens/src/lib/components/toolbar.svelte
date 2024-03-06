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
		background-color: #f8f9fa;
	}

	.navigation ul {
		list-style-type: none;
		margin: 0;
		padding: 0;
	}

	.navigation li button {
		display: block;
		color: black;
		text-align: center;
		padding: 14px 16px;
		text-decoration: none;
		background: none;
		border: none;
		cursor: pointer;
	}

	.navigation li button:hover {
		background-color: #ddd;
	}

	@media screen and (max-width: 900px) {
		.toolbar {
			display: block;
		}
	}
</style>
