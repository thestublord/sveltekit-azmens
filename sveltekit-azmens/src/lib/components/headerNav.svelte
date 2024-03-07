<nav class="navigation-header">
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

<style>
	.navigation-header {
		display: flex;
		justify-content: space-between;
		align-items: center;
		padding: 1rem;
		background-color: #793434;
		color: white;
	}
</style>
