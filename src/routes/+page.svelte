<script>
	import Image from './Image.svelte'
	let inputValue1 = 'オラに'
	let inputValue2 = '集中力'
	let inputValue3 = 'を分けてくれ'
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Joke App" />
</svelte:head>

<section>
	<h1>
		Joke App
	</h1>
</section>
<div class="img">
	<div>
		何をたのむ？
		<div><input bind:value={inputValue1} type="text" maxlength="6"/></div>
		<div><input bind:value={inputValue2} type="text" maxlength="6"/></div>
		<div><input bind:value={inputValue3} type="text" maxlength="6"/></div>
	</div>
	<Image
			msg1={inputValue1}
			msg2={inputValue2}
			msg3={inputValue3}
	/>
</div>


<style>
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 0.6;
	}

	h1 {
		width: 100%;
	}

	.img {
		text-align: center;
		max-width: 100vw;
	}

</style>
