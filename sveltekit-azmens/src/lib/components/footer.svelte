<footer>
	<div class="footer-images">
		<img src="/images/download.png" alt="Footer Image 1" class="footer-image" />
		<img src="/images/usag-region1-clr-w750-o.jpg" alt="Footer Image 2" class="footer-image" />
		<img src="/images/r1-logo-updated-2023-w652-o.jpg" alt="Footer Image 3" class="footer-image" />
		<img src="/images/logo-2.png" alt="Footer Image 4" class="footer-image footer-image-4" />
	</div>
</footer>

<style>
	footer {
		background-color: rgba(47, 47, 47, 0.5); /* Use rgba to specify the opacity */
		padding: 30px;
		text-align: center;
	}

	.footer-images {
		display: flex;
		justify-content: center;
	}

	.footer-image {
		width: 100px;
		height: 100px;
		margin: 0 20px;
	}

	.footer-image-4 {
		width: 200px;
		height: 100px;
		object-fit: cover;
	}

	@media (max-width: 900px) {
		.footer-image {
			width: 75px;
			height: 75px;
		}

		.footer-image-4 {
			width: 125px;
			height: 75px;
		}
	}
</style>
