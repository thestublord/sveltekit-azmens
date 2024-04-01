<script>
	import Events from '../../lib/components/events.svelte';
</script>

<div class="pageHeader" style="background-color: #30475e;">
	<div class="div1300">
		<div class="pageHeaderTitle">Upcoming Events</div>
		<div class="belowPageHeaderTitle"></div>
	</div>
</div>

<div class="breadcrumb">
	<!-- Breadcrumb content goes here -->
</div>

<Events />

<style>
	/* Add the following styles */

	.breadcrumb {
		padding: 2px;
		background-color: #f05454; /* Light grey background */
	}

	.pageHeader {
		padding: 50px 0;
	}

	.pageHeaderTitle {
		text-transform: uppercase;
		font-size: 5vw; /* Responsive font size */
		line-height: 1.1; /* Adjust line height */
		color: #fff;
		text-align: center;
	}

	@media screen and (max-width: 600px) {
		.pageHeaderTitle {
			font-size: 6vw; /* Increase font size on small screens */
		}
	}

	@media screen and (min-width: 601px) and (max-width: 1200px) {
		.pageHeaderTitle {
			font-size: 5vw; /* Decrease font size on medium screens */
		}
	}

	@media screen and (min-width: 1201px) {
		.pageHeaderTitle {
			font-size: 3vw; /* Decrease font size on large screens */
		}
	}
</style>
