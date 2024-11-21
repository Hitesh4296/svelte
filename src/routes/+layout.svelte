<script lang="ts">
	import '../app.css';
	let { children } = $props();
</script>

<main class="">
	<nav>
		<div class="fixed left-0 top-0 z-10 min-h-[72px] w-full backdrop-blur-[4px]"></div>
	</nav>

	<div class="px-[16px] pt-[72px] sm:px-[32px]">{@render children()}</div>
</main>
