<script>
	export let name;
	let src = 'hello-world/src/img/dancing-man-skillshare.gif';
	import Nested from './Nested.svelte';
	let string = `here's some <strong>HTML!!!</strong>`;
</script>

<main>
	<h1>Hello {name}!</h1>
	<p>Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn how to build Svelte apps.</p>
	<img {src} alt="{name}" />
	<Nested />
	<p>{@html string}</p>
	<input bind:value={name} placeholder="enter your name" />
<p>Hello {name || 'stranger'}!</p>
</main>

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

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>