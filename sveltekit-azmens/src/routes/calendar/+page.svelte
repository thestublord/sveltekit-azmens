<script>
	import Calendar from '../../lib/components/calendar.svelte';
</script>

<div class="pageHeader" style="background-color: #30475e;">
	<div class="div1300">
		<div class="pageHeaderTitle">Calendar</div>
	</div>
</div>

<div class="breadcrumb">
	<!-- Breadcrumb content goes here -->
</div>
<div class="container">
	<Calendar />
</div>

<style>
	/* Add the following styles */

	.container {
		margin: 0 auto;
	}

	.breadcrumb {
		padding: 2px;
		background-color: #dddddd; /* Light grey background */
	}

	.pageHeader {
		padding: 90px 0;
	}

	.pageHeaderTitle {
		text-transform: uppercase;
		font-size: 2.7em; /* Responsive font size */

		color: #fff;
		text-align: center;
	}

	@media screen and (max-width: 600px) {
		.pageHeaderTitle {
			font-size: 2em; /* Reduced font size for smaller screens */
		}
	}
</style>
