<footer>
	<div class="breadcrumb1">
		<!-- Breadcrumb content goes here -->
	</div>
	<div class="breadcrumb">
		<div class="footer-images">
			<a href="https://www.gymnastics.sport/site/" target="_blank">
				<img src="/images/download.png" alt="FIG" class="footer-image" />
			</a>
			<a href="https://usagym.org/" target="_blank">
				<img src="/images/usag-region1-clr-w750-o.jpg" alt="USA Gymnastics" class="footer-image" />
			</a>
			<a href="https://www.region1.men/" target="_blank">
				<img src="/images/r1-logo-updated-2023-w652-o.jpg" alt="Region One" class="footer-image" />
			</a>
		</div>

		<div class="breadcrumb-text">AZ Men's Gymnastics Association @ 2024.All Rights Reserved</div>
	</div>
</footer>

<style>
	footer {
		min-width: 300px;
	}

	.breadcrumb1 {
		padding: 12px;
		background-color: #222831;
	}

	.breadcrumb {
		padding: 18px;
		background-color: #30475e;
		display: flex;
		justify-content: space-between;
		align-items: center;
		flex-direction: row;
	}

	.breadcrumb-text {
		font-size: 0.9em;
		color: aliceblue;
	}

	.footer-images {
		display: flex;
		justify-content: center;
	}

	.footer-image {
		width: 50px;
		height: 50px;
		margin: 0 20px;
	}

	@media (max-width: 1200px) {
		.breadcrumb-text {
			font-size: 0.8em;
		}
	}

	@media (max-width: 900px) {
		.breadcrumb {
			flex-direction: column;
			align-items: center;
		}
		.breadcrumb-text {
			font-size: 0.8em;
			margin-right: 0;
			margin-top: 20px;
		}
		.footer-images {
			margin-top: 20px;
		}
		.footer-image {
			width: 45px;
			height: 45px;
		}
	}

	@media (max-width: 600px) {
		.footer-image {
			width: 50px;
			height: 50px;
			margin-bottom: 20px;
		}

		.breadcrumb-text {
			font-size: 0.8em;
		}
	}
</style>
