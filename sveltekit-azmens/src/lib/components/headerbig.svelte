<header>
	<div class="header-content">
		<!-- Wrap the image, text, and navigation inside a container -->
		<div class="logo-container">
			<!-- Wrap the image inside an anchor tag -->
			<a href="/" aria-label="Navigate to Home">
				<img
					src="/images/20k.png"
					alt="Arizona Men's Gymnastics Association Logo"
					class="left-image"
				/>
			</a>
			<!-- Position the text under the image -->
			<div class="header-text">
				<h1>AZ<br />Men's<br />Gymnastics<br />Association</h1>
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
	</div>
</header>

<style>
	header {
		position: fixed;
		top: 0;
		left: 0;
		width: 100%;
		background-color: #2f2f2f;
		padding: 20px 0;
		z-index: 100;
	}
</style>
