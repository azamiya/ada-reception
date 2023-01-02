<script>
	let name = '安谷屋　樹';
	let kanaName = 'あだにや　たつき';
	let description = '新郎';
</script>

<div
	class="relative flex items-center space-x-3 rounded-lg border border-gray-300 bg-white/80 px-6 py-5 shadow-sm"
>
	<div class="flex-shrink-0">
		<img
			class="h-10 w-10 rounded-full"
			src="https://images.unsplash.com/photo-1494790108377-be9c29b29330?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80"
			alt=""
		/>
	</div>
	<div class="min-w-0 flex-1">
		<div>
			<span class="absolute inset-0" aria-hidden="true" />
			<p class="text-[1rem] font-medium text-gray-900">{name}</p>
			<p class="text-[0.6rem] font-medium text-gray-900">{kanaName}</p>
			<p class="truncate text-sm text-gray-500">{description}</p>
		</div>
	</div>
</div>
