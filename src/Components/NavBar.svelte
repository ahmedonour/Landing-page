<script>
	import { fly } from 'svelte/transition';
	let visiaple = true;
	function toggelVisiple(){
		visiaple = !visiaple
	}
</script>

<nav>
	<div class="logo"><img src="../images/logo.svg" alt="The Compony Logo" /></div>
	<button on:click={toggelVisiple}><img src="../images/icon-menu.svg" alt="" /></button>
	{#if !visiaple}
	<ul in:fly={{ x: 1000, duration: 800 }} out:fly={{ x: 1000, duration: 500 }}>
	<button on:click={toggelVisiple}><img src="../images/icon-close-menu.svg" alt="" /></button>
		
		<li>Features</li>
		<li>Company</li>
		<li>Careers</li>
		<li>About</li>
		<div class="links">
			<a href="#" target="_blank" rel="noopener noreferrer">Login</a>
			<a href="#" class="reg">Register</a>
		</div>
	</ul>
	{/if}
</nav>

<style>
	nav {
		padding: 1rem;
		width: 100vw;
		height: 80px;
		display: flex;
		justify-content: space-between;
		align-items: center;
		/* box-shadow: 1px 1px 20px rgba(0, 0, 0, 0.1); */
	}
	nav ul {
		width: 70vw;
		height: 100vh;
		background: var(--Almost-White);
		color: var(--Medium-Gray);
		position: absolute;
		z-index: 99;
		display: flex;
		flex-direction: column;
		box-shadow: -130px 0px 10px rgba(0, 0, 0, 0.5);
		list-style: none;
		top: 0;
		right: 0;
	}
	nav ul li{
		padding: 1.5rem;
	}
	nav button {
		border: none;
		background-color: transparent;
	}
	nav ul button{
		position: absolute;
		top: 20px;
		right: 20px;
	}
	nav ul .links{
		width: 100%;
		height: 150px;
		display: grid;
		place-items: center;


	}
	nav ul .links a{
		color: var(--Medium-Gray);
		text-decoration: none;
	}
	nav ul .links .reg{
		display: grid;
		place-items: center;
		width: 90%;
		height: 3rem;
		border-radius: 15px;
		border: 2px solid var(--Medium-Gray);
	}
</style>
