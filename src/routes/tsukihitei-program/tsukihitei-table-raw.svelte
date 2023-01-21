<script>
	export let index;
	export let time;
	export let content;
	export let memo;

	console.log(index);
</script>

<tr class={index % 2 == 1 ? 'bg-white' : 'bg-gray-200'}>
	<td class="whitespace-nowrap py-4 pl-4 pr-3 text-xs font-medium text-gray-900 sm:pl-6">{time}</td>
	<td class="whitespace-nomal px-3 py-4 text-sm text-gray-500">{content}</td>
	<td class="whitespace-nomal px-3 py-4 text-sm text-gray-500">{memo}</td>
</tr>
