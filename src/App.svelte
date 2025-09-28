<script>
	let hex = randomHex();

	function randomHex() {
	    return '#' + Math.floor(Math.random()*16777215).toString(16).padStart(6, '0');
	}

	function change_color() {
	    hex = randomHex();
	}
</script>
<style lang="scss">
	@use "./style.scss";
</style>
<main style="background-color: {hex};">
	<p>{hex}</p>
	<button on:click={change_color}>
		Generate Random Number
	</button>
</main>
