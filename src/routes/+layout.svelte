<script>
	import '../app.css';
	import DarkModeSelector from '../components/DarkModeSelector.svelte';
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

<slot />
