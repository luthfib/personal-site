<script>
	import AppleMenuBar from './AppleMenuBar.svelte';
</script>

<div class="terminal">
	<div class="terminal-menubar">
		<AppleMenuBar />
	</div>
	<div>
		<p>~ ls programming languages</p>
		<ul>
			<li>python</li>
			<li>golang</li>
			<li>javascript</li>
		</ul>
		<p>~</p>
	</div>
</div>

<style lang="scss">
	.terminal {
		display: grid;
		grid-template-rows: 15px 1fr;
		border: 1px solid var(--primary-color);
		width: 80%;
		padding: 10px 5px 5px 15px;
		min-height: 250px;
		box-sizing: border-box;
		box-shadow: 0px 4px 6px -1px rgba(255, 255, 255, 0.06),
			0px 2px 4px -1px rgba(255, 255, 255, 0.08);
		border-radius: 8px;

		ul {
			list-style-type: none;
			padding: 0px 10px;
		}
	}
</style>
