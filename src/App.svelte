<script>
	let name = 'Svelte';
  let number = 50;
  let src = "https://i.pinimg.com/236x/fe/d3/fe/fed3fe3a113659f28c4de5c7d205fcc3--owl-shirt-owl-pictures.jpg";
  let altText = "Owl awsome";
  let htmlString = "<strong>This is strong text</strong> with <em>italick font</em>.";
</script>

<h1>Hello {name}!</h1>
<h2>{name.toUpperCase()}</h2>
<h2>{(Math.random()*number).toFixed(3)}</h2>
<img {src} alt={altText}>
<p>{@html htmlString}</p>

<style>
	:global(h1) {
		color: purple;
	}
  img {
    width: 100px;
    height: auto;
  }
</style>
