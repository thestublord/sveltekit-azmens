<script>
	import { goto } from '$app/navigation';

	function navigateTo(path) {
		return function (event) {
			if (event.type === 'click' || (event.type === 'keydown' && event.key === 'Enter')) {
				goto(path);
			}
		};
	}
</script>

<header>
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
</header>

<style>
	.header {
		position: fixed;
		top: 0;
		left: 0;
		right: 0;
		background-color: #2e2b3a;
		color: #fdfdfd;
		padding: 0.2rem;
		height: auto; /* Fixed height changed to auto */
		display: flex;
		align-items: center;
		justify-content: space-between;
		box-shadow: 0px 3px 6px 0px rgba(0, 0, 0, 0.16); /* Add this line */
	}
</style>
