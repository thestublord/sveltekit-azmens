<script>
	import Headerbig from './headerbig.svelte';
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

<div class="nav-container">
	<Toolbar />
</div>

<body>
	<header class="header">
		<div class="header-content">
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
							on:keydown={navigateTo('/important-links')}>More</button
						>
					</li>
				</ul>
			</nav>
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

		.nav-container {
			display: flex;
			justify-content: flex-end;
			width: 100%;
			margin-top: -10px; /* Move the nav-container up by 20px */
		}

		.header {
			position: fixed;
			top: 0;
			left: 0;
			right: 0;
			background-color: #222831;
			color: #fff6e0;
			padding: 0.5rem;
			height: auto; /* Fixed height changed to auto */
			display: flex;
			align-items: center;
			justify-content: space-between;
		}

		.header-content {
			display: flex;
			align-items: center;
			justify-content: space-between;

			text-align: center;
			width: 100%;
		}

		.navigation-header {
			display: flex;
			justify-content: center; /* Start in the middle by default */
			width: 100%;
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
			font-size: 18px;
			cursor: pointer;
			text-decoration: none;
			padding: 20;
		}

		nav button:hover {
			color: #f05454;
		}

		.navigation-header ul {
			display: flex;
			justify-content: space-between; /* Distribute items evenly by default */
			width: 100%;
		}

		@media screen and (min-width: 901px) {
			.header {
				position: static;
			}
			.navigation-header {
				display: flex;
				justify-content: center; /* Start in the middle by default */
				width: 100%;
			}
		}

		@media screen and (max-width: 900px) {
			.navigation-header {
				display: none; /* Hide the navigation header by default */
			}

			.header {
				position: fixed; /* Fix the position at smaller screens */
				top: 0; /* Align to the top of the viewport */
				left: 0; /* Align to the left of the viewport */
				width: 100%; /* Take up the full width of the viewport */
			}
		}
		@media screen and (min-width: 1201px) {
			.navigation-header ul {
				justify-content: center; /* Center the navigation links */
			}
		}
	</style>
</body>
