<script>
	
	import TheNav from '../components/TheNav.svelte';
	import Footer from '../components/Footer.svelte';
	import './styles.css';
    import TheMain from '../components/TheMain.svelte';
</script>


<div>
	<TheNav />
	<TheMain>
		<slot />
	</TheMain>
	<Footer />
</div>

<style>
	div {
		display: grid;
		grid-template-rows: auto 1fr auto;
		max-width: 1620px;
		padding: 1em;
		margin-left: auto;
		margin-right: auto;
		min-height: 100vh;
	}
</style>


