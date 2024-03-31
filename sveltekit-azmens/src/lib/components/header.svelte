<script>
	import { goto } from '$app/navigation';

	let showMenu = false;

	function toggleMenu() {
		showMenu = !showMenu;
	}

	function hideMenu() {
		showMenu = false;
	}

	function navigateTo(path) {
		goto(path);
		hideMenu();
	}

	$: {
		if (typeof document !== 'undefined') {
			if (showMenu) {
				document.body.style.overflow = 'hidden'; // Disable scrolling
			} else {
				document.body.style.overflow = 'auto'; // Enable scrolling
			}
		}
	}
</script>

<body>
	<header>
		<div class="logo" on:click={() => navigateTo('/')}>AZMGA</div>
		<nav>
			<ul class="nav-links">
				<li>
					<button
						type="button"
						on:click={() => navigateTo('/events')}
						on:keydown={() => navigateTo('/events')}>Events</button
					>
				</li>
				<li>
					<button
						type="button"
						on:click={() => navigateTo('/calendar')}
						on:keydown={() => navigateTo('/calendar')}>Calendar</button
					>
				</li>
				<li class="more">
					<button type="button">More</button>
					<ul class="submenu">
						<button
							type="button"
							on:click={() => navigateTo('/contact')}
							on:keydown={() => navigateTo('/contact')}>Contact</button
						>
						<button
							type="button"
							on:click={() => navigateTo('/about')}
							on:keydown={() => navigateTo('/about')}>About</button
						>
					</ul>
				</li>
			</ul>
		</nav>
		<div
			class={showMenu ? 'hamburger show' : 'hamburger'}
			on:click={toggleMenu}
			on:keydown={toggleMenu}
			role="button"
			tabindex="0"
		>
			<div class="line"></div>
			<div class="line"></div>
			<div class="line"></div>
		</div>

		<div class={showMenu ? 'popup-menu show' : 'popup-menu'}>
			<ul>
				<li><button on:click={() => navigateTo('/events')}>Events</button></li>
				<li><button on:click={() => navigateTo('/calendar')}>Calendar</button></li>
				<li><button on:click={() => navigateTo('/contact')}>Contact</button></li>
				<li><button on:click={() => navigateTo('/about')}>About</button></li>
				<!-- Add more menu items as needed -->
			</ul>
		</div>
	</header>

	<style>
		/* Add the following styles */

		body,
		html {
			margin: 0;
			padding: 0;
			box-sizing: border-box;
		}

		header {
			display: flex;
			justify-content: space-between;
			align-items: center;
			padding: 5px;
			background-color: #222831;
			color: white;
			box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1); /* Add shadow */
			height: 40px; /* Fixed height */
			position: relative; /* Add this line if not already present */
			z-index: 2; /* Add this line */
		}

		.logo {
			font-size: 18px;
			cursor: pointer;
			padding-left: 10px;
		}

		nav ul {
			list-style: none;
			display: flex;
		}

		nav ul li {
			margin-right: 25px;
		}

		nav ul li a {
			text-decoration: none;
			color: white;
		}

		button {
			background: none; /* Remove the background */
			border: none; /* Remove the border */
			color: white; /* Change the text color to white */

			cursor: pointer; /* Change the cursor to a pointer when hovering over the text */
			font-size: 18px; /* Increase the font size */
			padding: 0; /* Remove the padding */
		}

		button:hover {
			color: #f05454; /* Change the color when hovering over the button */
		}

		/* Styling for the submenu */
		.more:hover .submenu {
			display: block;
		}

		.submenu {
			display: none;
			position: absolute;
			background-color: #222831;
			padding: 20px;
			z-index: 1;
			margin-left: -35px;
			border-radius: 100px;
			border: 2px solid #dddddd;
		}

		.submenu li {
			margin: 1px 0;
		}

		/* Styling for the hamburger menu */
		.hamburger {
			display: none;
			flex-direction: column;
			cursor: pointer;
			position: relative;
			padding-right: 10px;
		}

		.hamburger .line {
			transition: all 0.3s ease;
		}

		.hamburger.show .line:nth-child(1) {
			transform: rotate(-45deg) translate(-5px, 6px);
		}

		.hamburger.show .line:nth-child(2) {
			opacity: 0;
		}

		.hamburger.show .line:nth-child(3) {
			transform: rotate(45deg) translate(-5px, -6px);
		}

		.line {
			width: 25px;
			height: 3px;
			background-color: white;
			margin: 3px 0;
		}

		nav {
			display: none;
		}

		nav.show {
			display: block;
		}

		@keyframes rollDown {
			0% {
				transform: translateY(-100%);
			}
			100% {
				transform: translateY(0);
			}
		}

		.popup-menu {
			padding-top: 110px; /* Add padding to the top */
			position: fixed;
			right: 0;
			top: 50px; /* Height of the header */
			bottom: 0; /* Stretch to the bottom */
			width: 100%; /* Full width */
			background-color: rgba(48, 71, 94, 0.9); /* Use rgba color model */
			animation: rollDown 0.5s forwards; /* Add roll down animation */
			display: none; /* Set a maximum height */
			overflow-y: auto; /* Make it scrollable */
			/* Add more styles as needed */
		}

		.popup-menu button {
			width: 300px; /* Adjust as needed */
			height: 100px; /* Adjust as needed */
			margin-top: 0; /* Remove the space above the button */
			margin-bottom: 0; /* Remove the space below the button */
			margin-left: auto;
			margin-right: auto;
			display: block; /* Needed for margin auto to work */
			background-color: #222831; /* Add the background color */
			color: white; /* Add the text color */
			border: 2px solid #dddddd; /* Add a 2px white border */
			border-radius: 10px; /* Add roundness to the buttons */
			opacity: 1; /* Keep the opacity as 1 */
			transition: background-color 0.3s ease; /* Add transition for smooth hover effect */
			/* Add more styles as needed */
		}

		.popup-menu button:hover {
			background-color: #dddddd; /* Change the background color on hover */
			color: #222831; /* Change the text color on hover */
		}

		.popup-menu.show {
			display: block; /* Show the menu when the 'show' class is added */
			animation: rollDown 0.5s forwards; /* Add roll down animation */
		}

		.popup-menu ul {
			list-style-type: none; /* Remove the bullet points */
			padding-left: 0; /* Remove the padding */
		}

		/* Media query for responsiveness */
		@media (max-width: 750px) {
			.nav-links {
				display: none;
			}

			.hamburger {
				display: flex;
			}
		}

		@media (min-width: 750px) {
			nav {
				display: block;
			}

			.hamburger,
			.popup-menu,
			.popup-menu.show {
				display: none;
			}
		}
	</style>
</body>
