<script>
	import '../app.css';
	import { base } from '$app/paths';

	let isMenuShown = false;

	function handleMenuClick() {
		isMenuShown = !isMenuShown;
	}

	function closeMenu() {
		isMenuShown = false;
	}

	const menu = [
		{ title: 'ホーム', link: `${base}/` },
		{ title: '日程', link: `${base}/schedule` },
		{ title: 'アクセス', link: `${base}/access` },
		{ title: 'ホテル情報', link: `${base}/hotel` },
		{ title: '参列者一覧', link: `${base}/attendee` },
		{ title: '仏前式　式次第', link: `${base}/wedding-program` },
		{ title: '仏前式の様子', link: `${base}/wedding-example` },
		{ title: '月日亭　式次第', link: `${base}/tsukihitei-program` },
		{ title: '月日亭　席次', link: `${base}/tsukihitei-seats` }
	];
</script>

<nav class="shadow relative z-50 mincho">
	<div class="mx-auto px-4 sm:px-6 lg:px-8 bg-slate-700 opacity-80 border-[1px] border-slate-500">
		<div class="flex h-16 justify-between">
			<div class="flex">
				<div class="flex flex-shrink-0 items-center">
					<p class="text-white text-sm">安谷屋家・岩﨑家 仏前式 御招待サイト</p>
				</div>
				<div class="hidden sm:ml-6 sm:flex sm:space-x-8">
					{#each menu as m}
						<a
							href={m.link}
							class="inline-flex items-center border-b-2 border-transparent px-1 pt-1 text-sm font-medium text-gray-500 hover:border-gray-300 hover:text-gray-700"
							>{m.title}</a
						>
					{/each}
				</div>
			</div>
			<div class="-mr-2 flex items-center sm:hidden">
				<!-- Mobile menu button -->
				<button
					type="button"
					on:click={handleMenuClick}
					class="inline-flex items-center justify-center rounded-md p-2 text-gray-400 hover:bg-gray-100 hover:text-gray-500 focus:outline-none focus:ring-2 focus:ring-inset focus:ring-blue-500"
					aria-controls="mobile-menu"
					aria-expanded="false"
				>
					<span class="sr-only">Open main menu</span>
					<!--
            Icon when menu is closed.

            Heroicon name: outline/bars-3

            Menu open: "hidden", Menu closed: "block"
          -->
					<svg
						class="block h-6 w-6"
						xmlns="http://www.w3.org/2000/svg"
						fill="none"
						viewBox="0 0 24 24"
						stroke-width="1.5"
						stroke="currentColor"
						aria-hidden="true"
					>
						<path
							stroke-linecap="round"
							stroke-linejoin="round"
							d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5"
						/>
					</svg>
					<!--
            Icon when menu is open.

            Heroicon name: outline/x-mark

            Menu open: "block", Menu closed: "hidden"
          -->
					<svg
						class="hidden h-6 w-6"
						xmlns="http://www.w3.org/2000/svg"
						fill="none"
						viewBox="0 0 24 24"
						stroke-width="1.5"
						stroke="currentColor"
						aria-hidden="true"
					>
						<path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" />
					</svg>
				</button>
			</div>
		</div>
	</div>

	<!-- Mobile menu, show/hide based on menu state. -->
	{#if isMenuShown}
		<div class="sm:hidden absolute bg-white right-0 w-1/2" id="mobile-menu">
			<div class="space-y-1 pt-2 pb-3">
				{#each menu as m}
					<a
						href={m.link}
						on:click={closeMenu}
						class="block border-l-4 border-transparent py-2 pl-3 pr-4 text-base font-medium text-gray-500 hover:border-gray-300 hover:bg-gray-50 hover:text-gray-700"
						>{m.title}</a
					>
				{/each}
			</div>
		</div>
	{/if}
</nav>

<slot />
