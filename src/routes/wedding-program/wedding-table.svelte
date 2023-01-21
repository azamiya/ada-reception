<script>
	import WeddingRaw from './wedding-table-raw.svelte';

	const programs = [
		{
			time: '9:00',
			content: '参列者集合',
			place: '本坊事務員 ※拝観料不要、入口で仏前式とお伝えください。'
		},
		{ time: '10:00', content: '仏前式　開式', place: '慈恩殿' },
		{ time: '10:50', content: '移動', place: '' },
		{ time: '11:00', content: '写真撮影', place: '' },
		{ time: '11:30', content: 'お経', place: '金堂' },
		{ time: '12:00', content: '仏前式　閉式', place: '' },
		{ time: '~', content: '順次タクシーにて月日亭へ移動', place: '' }
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
			<th scope="col" class="px-3 py-3.5 text-left text-sm font-semibold text-gray-900">場所</th>
		</tr>
	</thead>
	<tbody class="bg-white">
		{#each programs as program, i}
			<WeddingRaw index={i} time={program.time} content={program.content} place={program.place} />
		{/each}
	</tbody>
</table>

<style>
</style>
