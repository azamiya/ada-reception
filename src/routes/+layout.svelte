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
</script>

<nav class="shadow relative z-50 mincho">
	<div class="mx-auto px-4 sm:px-6 lg:px-8 bg-slate-700 opacity-80 border-[1px] border-slate-500">
		<div class="flex h-16 justify-between">
			<div class="flex">
				<div class="flex flex-shrink-0 items-center">
					<p class="text-white text-sm">安谷屋家・岩崎家 仏前式 御招待サイト</p>
				</div>
				<div class="hidden sm:ml-6 sm:flex sm:space-x-8">
					<!-- Current: "border-blue-500 text-gray-900", Default: "border-transparent text-gray-500 hover:border-gray-300 hover:text-gray-700" -->
					<a
						href="{base}/"
						class="inline-flex items-center border-b-2 border-transparent px-1 pt-1 text-sm font-medium text-gray-500 hover:border-gray-300 hover:text-gray-700"
						>ホーム</a
					>
					<a
						href="{base}/schedule"
						class="inline-flex items-center border-b-2 border-transparent px-1 pt-1 text-sm font-medium text-gray-500 hover:border-gray-300 hover:text-gray-700"
						>日程</a
					>
					<a
						href="{base}/access"
						class="inline-flex items-center border-b-2 border-transparent px-1 pt-1 text-sm font-medium text-gray-500 hover:border-gray-300 hover:text-gray-700"
						>アクセス</a
					>
					<a
						href="{base}/attendee"
						class="inline-flex items-center border-b-2 border-transparent px-1 pt-1 text-sm font-medium text-gray-500 hover:border-gray-300 hover:text-gray-700"
						>参列者紹介</a
					>
					<a
						href="{base}/adaniya-family"
						class="inline-flex items-center border-b-2 border-transparent px-1 pt-1 text-sm font-medium text-gray-500 hover:border-gray-300 hover:text-gray-700"
						>安谷屋家　連絡板</a
					>
					<a
						href="{base}/iwasaki-family"
						class="inline-flex items-center border-b-2 border-transparent px-1 pt-1 text-sm font-medium text-gray-500 hover:border-gray-300 hover:text-gray-700"
						>岩崎家　連絡板</a
					>
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
				<!-- Current: "bg-blue-50 border-blue-500 text-blue-700", Default: "border-transparent text-gray-500 hover:bg-gray-50 hover:border-gray-300 hover:text-gray-700" -->
				<a
					href="{base}/"
					on:click={closeMenu}
					class="block border-l-4 border-transparent py-2 pl-3 pr-4 text-base font-medium text-gray-500 hover:border-gray-300 hover:bg-gray-50 hover:text-gray-700"
					>ホーム</a
				>
				<a
					href="{base}/schedule"
					on:click={closeMenu}
					class="block border-l-4 border-transparent py-2 pl-3 pr-4 text-base font-medium text-gray-500 hover:border-gray-300 hover:bg-gray-50 hover:text-gray-700"
					>日程</a
				>
				<a
					href="{base}/access"
					on:click={closeMenu}
					class="block border-l-4 border-transparent py-2 pl-3 pr-4 text-base font-medium text-gray-500 hover:border-gray-300 hover:bg-gray-50 hover:text-gray-700"
					>アクセス</a
				>
				<a
					href="{base}/attendee"
					on:click={closeMenu}
					class="block border-l-4 border-transparent py-2 pl-3 pr-4 text-base font-medium text-gray-500 hover:border-gray-300 hover:bg-gray-50 hover:text-gray-700"
					>参列者紹介</a
				>
				<a
					href="{base}/wedding-program"
					on:click={closeMenu}
					class="block border-l-4 border-transparent py-2 pl-3 pr-4 text-base font-medium text-gray-500 hover:border-gray-300 hover:bg-gray-50 hover:text-gray-700"
					>仏前式　式次第</a
				>
				<a
					href="{base}/wedding-example"
					on:click={closeMenu}
					class="block border-l-4 border-transparent py-2 pl-3 pr-4 text-base font-medium text-gray-500 hover:border-gray-300 hover:bg-gray-50 hover:text-gray-700"
					>仏前式の様子</a
				>
				<a
					href="{base}/tsukihitei-program"
					on:click={closeMenu}
					class="block border-l-4 border-transparent py-2 pl-3 pr-4 text-base font-medium text-gray-500 hover:border-gray-300 hover:bg-gray-50 hover:text-gray-700"
					>月日亭　式次第</a
				>
				<a
					href="{base}/tsukihitei-seats"
					on:click={closeMenu}
					class="block border-l-4 border-transparent py-2 pl-3 pr-4 text-base font-medium text-gray-500 hover:border-gray-300 hover:bg-gray-50 hover:text-gray-700"
					>月日亭　席次</a
				>
				<a
					href="{base}/adaniya-family"
					on:click={closeMenu}
					class="block border-l-4 border-transparent py-2 pl-3 pr-4 text-base font-medium text-gray-500 hover:border-gray-300 hover:bg-gray-50 hover:text-gray-700"
					>安谷屋家　連絡板</a
				>
				<a
					href="{base}/iwasaki-family"
					on:click={closeMenu}
					class="block border-l-4 border-transparent py-2 pl-3 pr-4 text-base font-medium text-gray-500 hover:border-gray-300 hover:bg-gray-50 hover:text-gray-700"
					>岩崎家　連絡板</a
				>
			</div>
		</div>
	{/if}
</nav>

<slot />
