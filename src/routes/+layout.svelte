<script>
	import '$lib/styles/global.css';
	import SkipLink from './SkipLink.svelte';
</script>

<SkipLink />
<div class="wrapper body">
	<main tabindex="-1" id="main-content" class="stack copy">
		<slot />
	</main>
</div>
<footer class="wrapper">
	<div class="spread">
		<p class="font-bold mie-l">This is the footer.</p>
		<p>Copyright {new Date().getFullYear()}. All rights reversed.</p>
	</div>
</footer>

<style>
	.body {
		--wrapper-content-width: calc(6 * var(--layout-span) - var(--layout-gutter));
		background-color: var(--background-surface);
		padding-block: theme('spacing.xl-2xl-fixed');
	}

	footer {
		--gutter: 0;
		padding-block: theme('spacing.l-xl-fixed');
	}
</style>
