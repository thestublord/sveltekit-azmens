<div class="pageHeader" style="background-color: #30475e;">
	<div class="div1300">
		<div class="pageHeaderTitle">Contact</div>
		<div class="belowPageHeaderTitle"></div>
	</div>
</div>

<div class="breadcrumb">
	<!-- Breadcrumb content goes here -->
</div>

<div class="container">
	<div class="card">
		<p>
			<strong>Email:</strong>
			<a
				href="mailto:

			"
			>
				<!-- Email address goes here -->
			</a>
		</p>

		<h1>Send us a message</h1>

		<form class="form-container">
			<div class="text">
				<label for="name">Name:</label>
				<input type="text" id="name" name="name" required />

				<label for="email">Email:</label>
				<input type="email" id="email" name="email" required />

				<label for="message">Message:</label>
				<textarea id="message" name="message" required rows="5"></textarea>

				<button type="submit">Send</button>
			</div>
		</form>
	</div>
</div>

<style>
	/* Add the following styles */

	.container {
		margin: 0 auto;
		margin-top: 50px;
		max-width: 900px;
	}
	.form-container {
		display: flex;
		flex-direction: column;
		align-items: center;
		width: 100%;
		max-width: 500px;
		margin: 0 auto;
	}

	.form-container label,
	.form-container input,
	.form-container textarea,
	.form-container button {
		width: 100%;
		margin-bottom: 10px;
		box-sizing: border-box;
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
		padding: 100px 0;
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
</style>
