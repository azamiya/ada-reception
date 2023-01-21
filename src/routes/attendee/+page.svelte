<script>
	import { base } from '$app/paths';
	import Card from './card.svelte';
</script>

<div class="relative text-white mincho">
	<div class="absolute z-20 w-full">
		<h1 class="text-center text-xl mt-6 mb-6">参列者</h1>
		<div class="grid grid-cols-1 gap-4 grid-cols-2 mx-4">
			<Card
				name="安谷屋　樹"
				kanaName="あだにや　たつき"
				role="新郎"
				src="{base}/images/ada-face.png"
			/>
			<Card
				name="安谷屋　茜"
				kanaName="あだにや　あかね"
				role="新婦"
				src="{base}/images/akane-face.png"
			/>
			<Card
				name="安谷屋　薫"
				kanaName="あだにや　かおる"
				role="新郎/父"
				src="{base}/images/kaoru-face.png"
			/>
			<Card
				name="岩﨑　雅裕"
				kanaName="いわさき　まさひろ"
				role="新婦/父"
				src="{base}/images/masahiro-face.png"
			/>
			<Card
				name="安谷屋　盛"
				kanaName="あだにや　せい"
				role="新郎/弟"
				src="{base}/images/sei-face.png"
			/>
			<Card
				name="岩﨑　佐枝美"
				kanaName="いわさき　さえみ"
				role="新婦/母"
				src="{base}/images/saemi-face.png"
			/>
			<Card
				name="安谷屋 盛次郎"
				kanaName="あだにや せいじろう"
				role="新郎/祖父"
				src="{base}/images/seijiro-face.png"
			/>
			<Card
				name="岩﨑　裕介"
				kanaName="いわさき　ゆうすけ"
				role="新婦/兄"
				src="{base}/images/yuusuke-face.png"
			/>
			<Card
				name="安谷屋　米子"
				kanaName="あだにや　よねこ"
				role="新郎/祖母"
				src="{base}/images/yoneko-face.png"
			/>
			<Card
				name="岩﨑　美由紀"
				kanaName="いわさき　みゆき"
				role="新婦/義姉"
				src="{base}/images/miyuki-face.png"
			/>
			<Card
				name="安谷屋　豊"
				kanaName="あだにや　ゆたか"
				role="新郎/伯父"
				src="{base}/images/yutaka-face.jpg"
			/>
			<Card
				name="岩﨑　なの葉"
				kanaName="いわさき　なのは"
				role="新婦/姪"
				src="{base}/images/nanoha-face.png"
			/>
			<Card
				name="新垣　早苗"
				kanaName="あらかき　さなえ"
				role="新郎/伯母"
				src="{base}/images/sanae-face.png"
			/>
			<Card
				name="岩﨑　渓介"
				kanaName="いわさき　けいすけ"
				role="新婦/兄"
				src="{base}/images/keisuke-face.png"
			/>
			<Card
				name="新垣　幸祐"
				kanaName="あらかき　こうゆう"
				role="新郎/伯父"
				src="{base}/images/kouyu-face.png"
			/>
			<Card
				name="岩﨑　玲名"
				kanaName="いわさき　れいな"
				role="新婦/義姉"
				src="{base}/images/reina-face.png"
			/>
			<Card
				name="上原　桜"
				kanaName="うえはら　さくら"
				role="新郎/従姉妹"
				src="{base}/images/sakura-face.png"
			/>
			<Card
				name="岩﨑　岳流"
				kanaName="いわさき　たける"
				role="新婦/甥"
				src="{base}/images/takeru-face.png"
			/>
			<Card name="上原　憂也" kanaName="" role="新郎/従兄" src="{base}/images/yuuya-face.png" />
			<Card
				name="岩﨑　陽"
				kanaName="いわさき　はる"
				role="新婦/甥"
				src="{base}/images/haru-face.png"
			/>
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
