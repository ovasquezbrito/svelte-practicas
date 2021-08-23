<script lang="ts">
	let counter = 0;
	const increment = () => {
		counter++;
	};

	const decrement = () => {
		counter--;
	};
	const reset = () => {
		counter = 0;
	};
</script>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}
	h2 {
		font-size: 2rem;
	}
	.positive {
		color: olivedrab;
	}

	.negative {
		color: gray;
	}

	button {
		font-size: 2rem;
		margin: 0 0.4rem;
		border-radius: 5px;
	}

	button:hover {
		cursor: pointer;
	}

	.increment {
		background-color: #26d231;
	}

	.increment:active {
		background-color: #19b623;
	}

	.decrement {
		background-color: #3a9aea;
	}

	.decrement:active {
		background-color: #2688d8;
	}

	.reset {
		background-color: tomato;
	}

	.reset:active {
		background-color: #b64531;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>

<main>
	<h1>Counter App</h1>
	<hr />
	<h2 class={counter < 0 ? 'negative' : 'positive'}>Counter: {counter}</h2>
	<button class="increment" on:click={increment}>+1</button>
	<button class="decrement" on:click={decrement}>-1</button>
	<button class="reset" on:click={reset}>Reset</button>
</main>
