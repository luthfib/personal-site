<script>
</script>

<div class="menubar">
    <div class="menubar-close" />
    <div class="menubar-minimize" />
    <div class="menubar-fullscreen" />
</div>

<style lang="scss">
	
	.menubar div {
		cursor: pointer;
	}

	.menubar {
		display: flex;
		gap: 5px;

		:hover {
			opacity: 0.9;
		}
	}

	.menubar-close {
		background: var(--apple-red);
		width: 15px;
		height: 15px;
		border-radius: 50%;
	}

	.menubar-minimize {
		background: var(--apple-yellow);
		width: 15px;
		height: 15px;
		border-radius: 50%;
	}

	.menubar-fullscreen {
		background: var(--apple-green);
		width: 15px;
		height: 15px;
		border-radius: 50%;
	}
</style>
