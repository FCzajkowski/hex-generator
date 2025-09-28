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
	main{
		height:100vh;
		padding:0;
		margin:0;
		display:flex;
		align-items: center;
		justify-content: center;
		flex-direction: column;

	}
	p{
		font-size:30px;
		color:white;
		font-weight:900;

	}
	button{
		padding:13px 15px;
		background-color: transparent;
		border: 2px solid white;
		color:white;
		border-radius:20px;
		transition:250ms;
		font-weight:600;
	}
	button:hover{
		background-color: white;
		color:black;

		cursor:pointer;
	}
</style>
<main style="background-color: {hex};">
	<p>
		Your Random Color is: {hex}
	</p>
	<button on:click={change_color}>
		Generate Random Number
	</button>
</main>
