<script>
	import '../app.css';
	import DarkModeSelector from '$lib/components/DarkModeSelector.svelte';
	import { browser } from '$app/environment';

	let navHeight = 0;

	if (browser) {
		let nav = document.querySelector('nav');
		if (nav) {
			navHeight = nav.offsetHeight;
			console.log(navHeight);
		}
	}
</script>

<nav class="flex justify-between items-center p-2 dark:bg-zinc-900 shadow-md mb-2">
	<div class="flex justify-start space-x-4">
		<a href="/">Home</a>
		<a href="/projects">Projects</a>
		<a href="/about">About</a>
		<a href="/contact">Contact</a>
	</div>
	<div><DarkModeSelector /></div>
</nav>

<div id="content" class="px-2">
	<slot />
</div>

<footer class="flex justify-between items-center p-2 dark:bg-zinc-900 shadow-md mt-2" />

<style lang="postcss">
	#content {
		min-height: 100vh;
	}
</style>
