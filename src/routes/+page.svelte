<script>
	import Image from './Image.svelte'
	let inputValue = '集中力'
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
		何を分けてほしい？
		<input bind:value={inputValue} type="text" maxlength="6"/>
	</div>
	<Image msg={inputValue}/>
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
	}

</style>
