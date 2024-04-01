<div class="pageHeader" style="background-color: #30475e;">
	<div class="div1300">
		<div class="pageHeaderTitle">Contact</div>
		<div class="belowPageHeaderTitle"></div>
	</div>
</div>

<div class="breadcrumb">
	<!-- Breadcrumb content goes here -->
</div>

<body>
	<div class="container">
		<div class="card">
			<h1>Send us a message</h1>

			<h2>Email: example@example.com</h2>
		</div>
	</div>
</body>

<style>
	/* Add the following styles */

	body {
		/* Existing styles... */
		font-size: 1em; /* Set a base font size */
	}

	h1 {
		text-align: center;
		margin: 20px 0;
		color: #222831;
		font-size: 2em;
	}

	h2 {
		text-align: center;
		margin: 20px 0;
		color: #30475e;
		font-size: 1.6em;
	}

	body {
		display: flex;
		flex-direction: column;
		min-height: 100vh;
		margin: 0;
		padding: 0;
		font-family: 'Arial', sans-serif;
		font-size: 1em;
	}

	.container {
		margin: 0 auto;
		min-width: 200px;
		margin-top: 100px;
		margin-bottom: 100px;
	}

	.card {
		padding: 20px;
		background-color: #dddddd;
		box-shadow: 0 2px 5px rgba(0, 0, 0, 0.15);
		border-radius: 10px;
		max-width: 1200px;
		margin: 0 auto;
		color: #000;
	}

	.breadcrumb {
		padding: 2px;
		background-color: #f05454; /* Light grey background */
	}

	.pageHeader {
		padding: 50px 0;
	}

	.pageHeaderTitle {
		text-transform: uppercase;
		font-size: 4vw; /* Responsive font size */
		line-height: 1.1; /* Adjust line height */
		color: #fff;
		text-align: center;
	}

	@media screen and (max-width: 600px) {
		.pageHeaderTitle {
			font-size: 5vw; /* Increase font size on small screens */
		}
	}

	@media screen and (min-width: 601px) and (max-width: 1200px) {
		.pageHeaderTitle {
			font-size: 4vw; /* Decrease font size on medium screens */
		}
	}

	@media screen and (min-width: 1201px) {
		.pageHeaderTitle {
			font-size: 3vw; /* Decrease font size on large screens */
		}
	}

	@media (max-width: 900px) {
		h1 {
			font-size: 2.1em; /* Reduce the font size */
		}
	}

	@media (max-width: 600px) {
		h1 {
			font-size: 2.3em; /* Further reduce the font size */
		}
	}
</style>
