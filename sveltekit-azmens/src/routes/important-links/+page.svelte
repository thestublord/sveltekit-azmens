<script>
	import Video from '../../lib/components/video.svelte';
	import Pageheader from '../../lib/components/pageheader..svelte';
	import Eventsimage from '../../lib/components/eventsimage.svelte';
</script>

<div class="pageHeader" style="background-color: #30475e;">
	<div class="div1300">
		<div class="pageHeaderTitle">More</div>
		<div class="belowPageHeaderTitle"></div>
	</div>
</div>

<div class="breadcrumb">
	<!-- Breadcrumb content goes here -->
</div>

<div class="events-section">
	<Eventsimage />
</div>

<style>
	/* Add the following styles */
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
