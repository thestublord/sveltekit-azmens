<script>
	import emblaCarouselSvelte from 'embla-carousel-svelte';

	let emblaApi;
	let dots = [];

	function onInit(event) {
		emblaApi = event.detail;
		dots = new Array(emblaApi.slideNodes().length).fill(0).map((_, i) => i);
		console.log('Embla Carousel initialized');
		console.log('Dots:', dots);
	}

	function onSelect(index) {
		emblaApi.scrollTo(index);
	}
</script>

<div class="header-background">
	<h1>Upcoming Events</h1>
</div>

<div class="embla" use:emblaCarouselSvelte on:init={onInit} on:select={onSelect}>
	<div class="embla__container">
		<div class="embla__slide">
			<a href="http://www.mensregion1champ.com/">
				<img src="/images/My first design (10).png" alt="Slide 1" />
			</a>
		</div>
		<div class="embla__slide">
			<a href="https://usagym.org/events/2024-mens-western-championships/">
				<img src="/images/ezgif-6-470b8d7d72.jpg" alt="Slide 2" />
			</a>
		</div>
		<div class="embla__slide">
			<a href="https://usagym.org/events/2024-mens-development-program-national-championships/">
				<img src="/images/ezgif-6-51a5568cf5.jpg" alt="Slide 3" />
			</a>
		</div>
	</div>
</div>

<div class="bar"></div>
<div class="bar"></div>

<div class="embla-dots">
	{#each dots as dot (dot)}
		<button
			class="embla-dot {emblaApi && emblaApi.selectedScrollSnap() === dot ? 'is-selected' : ''}"
			on:click={() => onSelect(dot)}
		></button>
	{/each}
</div>

<style>
	/* Add the following styles */

	.bar {
		height: 2px; /* Height of the bar */
		background-color: #000; /* Color of the bar */
		margin: 10px 0; /* Space above and below the bar */
	}

	h1 {
		text-align: center;
		color: #032645;
		margin-top: 100px;
		margin-bottom: 50px; /* Add this line */
		font-size: 2em; /* Default size */
	}

	.embla {
		position: relative;
		overflow: hidden;
		width: 100%;
		z-index: 0; /* Ensure it's behind the orange bar */
	}

	.embla__container {
		display: flex;
	}
	.embla__slide {
		flex: 0 0 100%;
		min-width: 0;
	}

	.embla-dot {
		background: #000000; /* Change the color to black */
		border: none;
		border-radius: 50%;
		width: 20px; /* Increase the size to 20px */
		height: 20px; /* Increase the size to 20px */
		margin: 0 5px;
		cursor: pointer;
		z-index: 1000; /* Ensure it's above other elements */
	}

	.embla-dots {
		display: flex;
		justify-content: center;
		position: relative; /* Add this line */
		z-index: 1000; /* Ensure it's above other elements */
	}

	.embla__slide img {
		width: 100%;
		height: auto; /* Adjusted height */
		object-fit: cover;
		transition: transform 0.3s ease; /* Add this line */
		transform: scale(0.9); /* Make the images smaller */
	}

	.embla__slide img:hover {
		transform: scale(1); /* Zoom in to the original size */
	}

	@media screen and (min-width: 900px) {
		.embla__slide img {
			max-width: 900px;
			margin: auto; /* Center the images */
		}
	}
</style>
