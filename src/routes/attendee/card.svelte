<script>
	export let name;
	export let kanaName;
	export let role;
	export let src;
</script>

<div
	class="{!name &&
		'opacity-0'} relative flex items-center space-x-3 rounded-lg border border-gray-300 bg-white/80 px-2 py-2 shadow-sm"
>
	<div class="flex-shrink-0">
		<img class="h-10 w-10 rounded-full" {src} alt="" />
	</div>
	<div class="min-w-0 flex-1">
		<div>
			<span class="absolute inset-0" aria-hidden="true" />
			<p class="text-[0.9rem] font-medium text-gray-900">{name}</p>
			<p class="text-[0.6rem] font-medium text-gray-900">{kanaName}</p>
			<p class="truncate text-[0.75rem] text-gray-500">{role}</p>
		</div>
	</div>
</div>
