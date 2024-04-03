<div>
	<div class="card">
		<div class="card-header">
			<h2>{title}</h2>
		</div>
		<div class="card-body">
			{#if image}
				<img src={image} alt={title} />
			{/if}
			<p>{content}</p>
		</div>
	</div>
</div>
;

<style>
	/* Add the following styles */

	.card {
		border: 1px solid #ccc;
		border-radius: 5px;
		margin: 10px;
		padding: 10px;
	}

	.card-header {
		background-color: #f1f1f1;
		border-bottom: 1px solid #ccc;
		padding: 10px;
	}

	.card-body {
		padding: 10px;
	}

	img {
		max-width: 100%;
		height: auto;
	}
</style>
