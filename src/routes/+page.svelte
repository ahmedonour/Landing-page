<script>
	import ClientLogo from '../Components/clientLogo.svelte';
	import HeroImage from '../Components/heroImage.svelte';
	import NavBar from '../Components/NavBar.svelte';
	import Text from '../Components/Text.svelte';
</script>

<main>
	<NavBar />
	<HeroImage />
	<Text />
	<ClientLogo />
</main>

<style>
	main {
		height: fit-content;
	}
</style>
