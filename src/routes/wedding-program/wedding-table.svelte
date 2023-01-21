<script>
	import WeddingRaw from './wedding-table-raw.svelte';

	const programs = [
		{
			time: '9:00',
			content: '参列者集合',
			memo: '本坊事務員 ※拝観料不要、入口で仏前式とお伝えください。'
		},
		{ time: '10:00', content: '仏前式　開式', memo: '慈恩殿' },
		{ time: '10:50', content: '移動', memo: '' },
		{ time: '11:00', content: '写真撮影', memo: '' },
		{ time: '11:30', content: 'お経', memo: '金堂' },
		{ time: '12:00', content: '仏前式　閉式', memo: '' },
		{ time: '~', content: 'タクシーにて月日亭へ移動', memo: '月日亭手配' }
	];
</script>

<table class="w-full divide-y divide-gray-300 text-xs table-fixed break-all">
	<thead class="bg-gray-50">
		<tr>
			<th
				scope="col"
				class="py-3.5 pl-4 pr-3 text-left text-xs font-semibold text-gray-900 sm:pl-6 w-16">時間</th
			>
			<th scope="col" class="px-3 py-3.5 text-left text-sm font-semibold text-gray-900">内容</th>
			<th scope="col" class="px-3 py-3.5 text-left text-sm font-semibold text-gray-900">備考</th>
		</tr>
	</thead>
	<tbody class="bg-white">
		{#each programs as program, i}
			<WeddingRaw index={i} time={program.time} content={program.content} memo={program.memo} />
		{/each}
	</tbody>
</table>

<style>
</style>
