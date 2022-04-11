<script>
	import '$lib/globalStyles.css';
	import Card from '$lib/card.svelte';
</script>

<svelte:head>
	<title>Preview Card</title>
</svelte:head>

<main class="container">
	<Card
		image="/icon-sedans.svg"
		alt="sedan"
		heading="sedans"
		text="Choose a sedan for its affordability and excellent fuel economy. Ideal for cruising in the city or on your next road trip."
		buttonText="learn more"
		bgcolor="orange"
	/>
	<Card
		image="/icon-suvs.svg"
		alt="suv"
		heading="suvs"
		text="Take an SUV for its spacious interior, power, and versatility. Perfect for your next family vacation and off-road adventures."
		buttonText="learn more"
		bgcolor="cyan"
	/>
	<Card
		image="/icon-luxury.svg"
		alt="luxury"
		heading="luxury"
		text="Cruise in the best car brands without the bloated prices. Enjoy the enhanced comfort of a luxury rental and arrive in style. "
		buttonText="learn more"
		bgcolor="darkCyan"
	/>
</main>

<style>
	.container {
		background-color: var(--gray);
	}
	@media screen and (min-width: 48.0625rem) {
		.container {
			display: grid;
			place-content: center;
			grid-auto-flow: column;
			height: 100vh;
		}
	}
</style>
