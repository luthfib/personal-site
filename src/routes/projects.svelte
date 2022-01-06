<script context="module">
	export const prerender = true;
</script>

<script>
	const numberOfLines = 30;

	const work = {
		lastProject: {
			name: 'Registration System',
			year: "In progress",
			techStack: ['Nextjs', 'Python', 'Serverless API', 'MongoDB', "Vercel"],
			description: 'Registration system for an event hosting 1000+ participants from 20+ nations'
		},
		smallBusiness: {
			name: 'Language Service Solutions',
			year: "2021",
			techStack: ['Nextjs', 'Styled JSX', "Vercel"],
			description:
				'Modernized small business website to have better web vitals and overall modern look'
		},
		NonProfit: {
			name: 'Borneo Football',
			year: "2017",
			techStack: ['Nextjs', 'Styled JSX', "Vercel"],
			description:
				'Modernized small business website to have better web vitals and overall modern look'
		}
	};
</script>

<svelte:head>
	<title>Skills</title>
</svelte:head>

<section class="ide-content">
	<div class="line-numbers">
		{#each Array(numberOfLines) as _, i}
			<div>{i + 1}</div>
		{/each}
	</div>
	<div class="code">
		{#each Object.entries(work) as [key, obj], i}
			<div>
				<p class="scope">const &nbsp;</p>
				<p class="variable">{key} &nbsp;</p>
				<p class="space">= &nbsp;</p>
				<p class="object">{`{}`}</p>
			</div>
			{#each Object.entries(obj) as [attribute, value], innerIdx}
				<div class="code-line">
					<p class="variable">{key}.{attribute}</p>
					<p class="space">&nbsp; = &nbsp;</p>
					<p class="value">{value}</p>
				</div>
			{/each}
			<div />
		{/each}
	</div>
</section>

<style lang="scss">
	section {
		--num-of-lines: 1;
	}

	.ide-content {
		display: grid;
		grid-template-columns: 30px 1fr;
	}

	.code {
		display: flex;
		flex-direction: column;
		padding: 10px;

		> div {
			height: 30px;
			display: flex;
			align-items: center;
		}

		&-line {
			display: flex;
		}

		.variable {
			color: var(--blue-2);
		}

		.space {
			color: var(--white);
		}

		.value {
			color: var(--green-1);
		}

		.scope {
			color: var(--blue-1);
		}

		.object {
			color: var(--yellow-1);
		}
	}

	.line-numbers {
		background: var(--accent-1);
		display: flex;
		flex-direction: column;
		align-items: center;
		font-size: 1rem;
		padding: 10px;

		> div {
			height: 30px;
			display: flex;
			align-items: center;
		}
	}
</style>
