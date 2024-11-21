<script lang="ts">
	interface Props {
		containerClass?: string;
		textBlockClass?: string;
	}
	let { containerClass, textBlockClass } = $props() as Props;
</script>

<div
	class="animate-door flex h-[120px] w-[120px] flex-none items-center justify-center rounded-full bg-[#fff312] pl-[24px] sm:h-[180px] sm:w-[180px] {containerClass}"
	style="border: 1px solid rgba(255,255,255,0.1); box-shadow: 0px 0px 150px 75px rgba(245,223,77,0.1);"
>
	<div
		class="mb-[10px] grid h-fit w-full -skew-x-[24deg] grid-cols-4 place-items-baseline gap-[2px] p-[12px] {textBlockClass}"
	>
		<div class="h-[70px] w-full rounded-tl-[40px] bg-black bg-repeat sm:h-[90px]"></div>
		<div class="h-[45px] w-full self-end rounded-tr-[40px] bg-black sm:h-[60px]"></div>

		<div class="h-[45px] w-full rounded-tl-[40px] bg-black sm:h-[60px]"></div>
		<div class="h-[45px] w-full rounded-tr-[40px] bg-black sm:h-[60px]"></div>
	</div>
</div>

<style>
	.animate-door {
		animation: door 0.3s linear;
		perspective-origin: -100% 100%;
	}

	@keyframes door {
		0% {
			transform: rotateY(-30deg);
			opacity: 0;
		}
		100% {
			transform: rotateY(0deg);
			opacity: 1;
		}
	}
</style>
