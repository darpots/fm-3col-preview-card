<script>
	export let image;
	export let alt;
	export let heading;
	export let text;
	export let buttonText;
	export let bgcolor;
</script>

<section style="--bg: var(--{bgcolor})">
	<div class="container">
		<div class="image"><img src={image} {alt} /></div>
		<h1>{heading}</h1>
		<p>{text}</p>
		<div>
			<button style="--bg: var(--{bgcolor})">
				{buttonText}
			</button>
		</div>
	</div>
</section>

<style>
	section {
		background-color: var(--bg);
		padding: 3rem;
	}
	section:first-of-type {
		border-radius: 0.5rem 0.5rem 0 0;
	}
	section:last-of-type {
		border-radius: 0 0 0.5rem 0.5rem;
	}
	.container {
		max-width: 14.4375rem;
		margin: 0 auto;
	}
	.image {
		margin-bottom: 2.1875rem;
	}

	h1 {
		text-transform: uppercase;
		color: var(--gray);
		font-family: 'Big Shoulders Display', cursive;
		font-weight: 700;
		font-size: 2.5rem;
		line-height: 3rem;
		margin-bottom: 1.5625rem;
	}
	p {
		font-family: 'Lexend Deca', sans-serif;
		font-size: 0.9375rem;
		line-height: 1.5625rem;
		color: var(--white);
		mix-blend-mode: normal;
		opacity: 0.75;
		margin-bottom: 1.5625rem;
	}
	button {
		border-radius: 1.5625rem;
		background-color: var(--gray);
		font-family: 'Lexend Deca';
		font-size: 0.9375rem;
		line-height: 1.5625rem;
		border: 0;
		color: var(--bg);
		padding: 0.625rem 1.875rem;
		text-transform: capitalize;
		border: 0.125rem var(--gray) solid;
	}
	button:hover {
		background-color: transparent;
		color: var(--gray);
		border: 0.125rem var(--gray) solid;
	}

	@media screen and (min-width: 64rem) {
		.container {
			max-width: 13.25rem;
		}
		.image {
			margin-bottom: 2.1875rem;
		}
		h1 {
			margin-bottom: 1.5625rem;
		}
		p {
			margin-bottom: 5.1875rem;
		}
		section:first-of-type {
			border-radius: 0.5rem 0 0 0.5rem;
		}
		section:last-of-type {
			border-radius: 0 0.5rem 0.5rem 0;
		}
	}
</style>
