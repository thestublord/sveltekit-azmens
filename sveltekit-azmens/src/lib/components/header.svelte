<script>
	import Toolbar from './toolbar.svelte';
	import { goto } from '$app/navigation';

	function navigateTo(path) {
		return function (event) {
			if (event.type === 'click' || (event.type === 'keydown' && event.key === 'Enter')) {
				goto(path);
			}
		};
	}
</script>

<body>
	<header class="header">
		<div class="header-content">
			<div class="logo-container">
				<a href="/" aria-label="Navigate to Home">
					<img
						src="/images/20k.png"
						alt="Arizona Men's Gymnastics Association Logo"
						class="left-image"
					/>
				</a>
				<div class="header-text">
					<h1>AZ<br />Men's<br />Gymnastics<br />Association</h1>
				</div>
			</div>

			<nav class="navigation-header">
				<ul>
					<li>
						<button type="button" on:click={navigateTo('/')} on:keydown={navigateTo('/')}
							>Home</button
						>
					</li>
					<li>
						<button
							type="button"
							on:click={navigateTo('/events')}
							on:keydown={navigateTo('/events')}>Events</button
						>
					</li>
					<li>
						<button
							type="button"
							on:click={navigateTo('/calendar')}
							on:keydown={navigateTo('/calendar')}>Calendar</button
						>
					</li>
					<li>
						<button
							type="button"
							on:click={navigateTo('/important-links')}
							on:keydown={navigateTo('/important-links')}>Important Links</button
						>
					</li>
				</ul>
			</nav>

			<Toolbar />
		</div>
	</header>

	<main class="main-content">
		<!-- Main content here -->
	</main>

	<style>
		body,
		html {
			margin: 0;
			padding: 0;
		}

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
			justify-content: flex-end; /* Add this line */
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
			color: white;
			font-size: 20px;
			cursor: pointer;
			text-decoration: none;
			padding: 0;
		}

		nav button:hover {
			color: #fe545d;
		}
		.left-image {
			width: 70px; /* Adjust this value as needed */
			height: auto; /* Maintain aspect ratio */
			margin-right: 8px; /* Add this line */
			float: left;
		}

		.header-text {
			text-align: center;
			width: 90%;
			font-size: 0.8em; /* Add this line */
			margin-right: 0;
		}

		@media screen and (min-width: 901px) {
			.header {
				position: static;
				top: 0;
				left: 0;
				right: 0;
				background-color: #2e2b3a;
				color: #fdfdfd;
				padding: 0.2rem;
				height: 60px; /* Set a fixed height */
		}
			
			.navigation-header {
				z-index: 1; /* Make sure the navigation header is above other elements */
				display: none; /* Hide navigation-header by default */
				justify-content: flex-end; /* Add this line */
			}

			.header-text {
				display: inline-block; /* Ensure the header text is displayed */
			}

			nav ul {
				justify-content: center; /* Center the navigation links */
			}

			nav li {
				margin: 0 2rem; /* Increase the margin */
			}
		}

		@media screen and (max-width: 900px) {
			.header-text {
				display: none; /* Hide the header text */
			}

			.header {
				position: fixed;
				top: 0;
				left: 0;
				right: 0;
				background-color: #2e2b3a;
				color: #fdfdfd;
				padding: 0.2rem;
				height: 60px; /* Set a fixed height */
		}
	</style>
</body>
