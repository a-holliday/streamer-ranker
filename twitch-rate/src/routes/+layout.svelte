<script>

	// Your selected Skeleton theme:
	import '@skeletonlabs/skeleton/themes/theme-skeleton.css';

	// This contains the bulk of Skeletons required styles:
	import '@skeletonlabs/skeleton/styles/skeleton.css';
						
	import Header from './Header.svelte';
	import './styles.css';
	import '../app.css';

	const modal = {
		type: 'confirm',
		title: 'Are you sure?',
		body: 'This is a modal dialog.',
	};

	const handleOpen = () => {
		modalStore(modal).trigger();
	};

	const handleClose = () => {
		modalStore(modal).trigger();
	}


</script>

<div class="app">
	<Header />

	<main>
		<slot />
	</main>

	<footer>
		<p>visit <a href="https://www.twitch.tv/toluafo">ToluAfo</a> to learn about being a human.</p>
	</footer>
</div>

<style>
	.app {
		display: flex;
		flex-direction: column;
		min-height: 100vh;
	}

	main {
		flex: 1;
		display: flex;
		flex-direction: column;
		padding: 1rem;
		width: 100%;
		max-width: 64rem;
		margin: 0 auto;
		box-sizing: border-box;
	}

	footer {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		padding: 12px;
	}

	footer a {
		font-weight: bold;
	}

	@media (min-width: 480px) {
		footer {
			padding: 12px 0;
		}
	}
</style>
