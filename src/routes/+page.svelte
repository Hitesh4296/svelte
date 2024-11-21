<script>
	import Logo from '$lib/Logo.svelte';
</script>

<main>
	<div class="relative mx-auto flex h-screen w-full max-w-[1440px] items-center justify-center">
		<div class="flex h-full min-w-[60vw] items-center">
			<div
				class="top:50% left:50% absolute z-[-1] flex h-[400px] w-full items-center justify-center overflow-hidden px-[36px] sm:min-w-[60vw]"
			>
				<div
					class="grid h-[300px] w-full -skew-x-[24deg] grid-cols-4 place-items-end gap-[12px] px-[0px] sm:h-[400px] sm:px-[64px]"
				>
					<div class="moving-dots h-full w-full rounded-tl-[100px]"></div>
					<div class="moving-dots h-[66%] w-full rounded-tr-[100px]"></div>
					<div class="moving-dots h-[66%] w-full rounded-tl-[100px]"></div>
					<div class="moving-dots h-[66%] w-full rounded-tr-[100px]"></div>
				</div>
			</div>

			<div
				class="flex min-h-[200px] flex-col justify-center gap-[24px] px-[40px] sm:min-h-[400px] sm:flex-row"
			>
				<div class="z-[2]">
					<Logo />
				</div>

				<div>
					<h1 class="text-4xl font-bold">I'm Hitesh Narwal</h1>
					<p>
						and I've been building on the web for over 5.5 years at places like Virtualness (now,
						Verix) and Nykaa Fashion,
					</p>
					<div></div>
				</div>
			</div>
		</div>
	</div>

	<div class="w-full"></div>
</main>

<style>
	.moving-dots {
		--size: 12px;
		overflow: hidden;
		position: relative;

		&::before {
			content: '';
			position: absolute;
			width: 200%;
			height: 200%;
			z-index: -1;
			animation: moveDots 4s linear infinite;
			transform: skewX(12deg);
			background: radial-gradient(circle, #fff312 10%, transparent 10%) 0 0 / var(--size)
				var(--size);
		}
	}

	@keyframes moveDots {
		0% {
			background-position: 0 0;
		}
		100% {
			background-position: calc(var(--size) * 1) 0;
		}
	}
</style>
