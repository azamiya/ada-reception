<script>
	import TsukihiteiTableRaw from './tsukihitei-table-raw.svelte';

	const programs = [
		{
			time: '13:00',
			content: '薬師寺からタクシー移動',
			memo: 'イベントで奈良公園混んでいる可能性あり'
		},
		{ time: '13:45', content: '月日亭到着', memo: '控室に軽食を用意（三笠、柿の葉寿司、お茶）' },
		{ time: '14:00', content: 'ロケーションフォト撮影', memo: '新婦は白無垢にて' },
		{ time: '15:00', content: '撮影終了、お色直し', memo: '' },
		{ time: '15:30', content: '開宴', memo: '' },
		{ time: '', content: '新郎新婦入場', memo: '' },
		{ time: '', content: '開演の辞', memo: '' },
		{ time: '', content: 'ウェルカムスピーチ', memo: '新郎' },
		{ time: '', content: '乾杯', memo: '新郎/父' },
		{ time: '', content: 'プロフィールムービー', memo: '' },
		{ time: '', content: '親族紹介', memo: '安谷屋　盛、岩﨑　裕介' },
		{ time: '', content: '記念品贈呈', memo: '新郎、新婦' },
		{ time: '', content: 'お手紙朗読', memo: '新婦' },
		{ time: '', content: '両家代表謝辞', memo: '新婦/父' },
		{ time: '17:30', content: 'おひらきの辞', memo: '' },
		{ time: '', content: '送賓', memo: 'タクシー6台 月日亭手配' }
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
			<TsukihiteiTableRaw
				index={i}
				time={program.time}
				content={program.content}
				memo={program.memo}
			/>
		{/each}
	</tbody>
</table>

<style>
</style>
