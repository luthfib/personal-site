<script>
	import '../app.css';
	import Terminal from '$lib/Terminal.svelte';
	import AppleMenuBar from '$lib/AppleMenuBar.svelte';
	import { page } from '$app/stores';
</script>

<main>
	<section class="common-section">
		<div class="about-me-container">
			<div class="about-me">
				<h1>Luthfi Bustillos</h1>
				<p>I am Colombian full-stack developer, residing in the United States</p>
				<p>
					I am most interested in building innovative user experiences and giving users that wow
					experience
				</p>
			</div>
		</div>
		<div class="terminal-container">
			<Terminal />
		</div>
		<footer>
			<p>luthfib@hey.com</p>
		</footer>
	</section>
	<section class="ide">
		<div class="top-bar">
			<AppleMenuBar />
			<ul class="tabs">
				<div>
					<li class:active={$page.url.pathname === '/'}>
						<a sveltekit:prefetch href="/">Experience.md</a>
					</li>
					<div />
				</div>
				<li class:active={$page.url.pathname === '/projects'}>
					<a sveltekit:prefetch href="/projects">Projects.js</a>
				</li>
				<li class:active={$page.url.pathname === '/skills'}>
					<a sveltekit:prefetch href="/skills">skills.py</a>
				</li>
				<li class:active={$page.url.pathname === '/education'}>
					<a sveltekit:prefetch href="/education">Education.go</a>
				</li>
			</ul>
		</div>

		<slot />
	</section>
</main>

<style lang="scss">
	main {
		display: grid;
		grid-template-columns: 1fr 1fr;
		width: 100%;
		box-sizing: border-box;
		height: 100%;
	}

	.top-bar {
		padding: 10px;
		display: flex;
		align-items: center;
		padding-bottom: 0px;

		ul {
			list-style: none;
			display: flex;
			gap: 10px;
			margin: 0px;

			li {
				border: 1px solid var(--accent-2);
				border-radius: 6px 6px 0px 0px;
				border-bottom: 1px solid var(--background);
				padding: 8px 12px;
				margin-top: 4px;
				z-index: 10;
				position: relative;
			}

			li:after {
				content: ' ';
			}
		}

		border-bottom: 1px solid var(--accent-2);
	}

	.ide {
		display: grid;
		grid-template-rows: 50px 1fr;
	}

	.terminal-container {
		display: flex;
		justify-self: baseline;
		width: 100%;
	}

	.about-me {
		margin: auto;
		width: 80%;
	}

	.common-section {
		display: grid;
		grid-template-rows: 1fr 1fr;
		padding: 4rem;
		height: 100%;
		border-right: 1px solid var(--accent-2);
	}

	.common-section h1 {
		color: var(--secondary-white);
	}

	footer {
		display: flex;
		flex-direction: column;
		justify-content: baseline;
		align-items: center;
		padding: 40px;
	}

	@media (min-width: 480px) {
		footer {
			padding: 40px 0;
		}
	}
</style>
