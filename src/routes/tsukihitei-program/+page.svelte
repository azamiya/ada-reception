<script>
	import { base } from '$app/paths';
	import TsukihiteiTable from './tsukihitei-table.svelte';
</script>

<div class="relative text-white mincho">
	<div class="absolute z-20 w-full">
		<h1 class="text-center text-lg mt-6 mb-2">月日亭　小宴　式次第</h1>

		<div class="m-4">
			<TsukihiteiTable />
		</div>
	</div>

	<div class="img-container absolute w-full">
		<div class="absolute z-10 w-full bg-gray-800 opacity-50 h-[100%]" />
		<img alt="9435" class="z-0" src="{base}/images/9435.jpg" />
		<img alt="9435" class="z-0" src="{base}/images/9435.jpg" />
	</div>
</div>

<style>
	div.img-container {
		top: 0rem;
	}
</style>
