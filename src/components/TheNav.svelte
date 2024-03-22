<script>
	import { page } from '$app/stores';
</script>
<nav>
	<a class="home" href="/">
		<img width="28" src="/icons/home.svg" alt="Home">
	</a>
	<ul>

		
		<li aria-current={$page.url.pathname === '/' ? 'page' : undefined}>
		</li>
		<li aria-current={$page.url.pathname === '/lunes' ? 'page' : undefined}>
			<a href="/lunes">Lunes</a>
		</li>
		<li aria-current={$page.url.pathname === '/martes' ? 'page' : undefined}>
			<a href="/martes">Martes</a>
		</li>
		<li aria-current={$page.url.pathname === '/miercoles' ? 'page' : undefined}>
			<a href="/miercoles">Miércoles</a>
		</li>
		<li aria-current={$page.url.pathname === '/jueves' ? 'page' : undefined}>
			<a href="/jueves">Jueves</a>
		</li>
		<li aria-current={$page.url.pathname === '/viernes' ? 'page' : undefined}>
			<a href="/viernes">Viernes</a>
		</li>
		<li aria-current={$page.url.pathname === '/sabado' ? 'page' : undefined}>
			<a href="/sabado">Sábado</a>
		</li>
		<li aria-current={$page.url.pathname === '/domingo' ? 'page' : undefined}>
			<a href="/domingo">Domingo</a>
		</li>
		
	</ul>
</nav>





<style>
	

	nav {
		display: flex;
		justify-content: space-between;
		--background: rgb(255 255 255 / 15%);
		background-color: var(--background);
		border-radius: .5rem;
	}


	ul {
		position: relative;
		padding: 0;
		margin: 0;
		height: 3em;
		display: flex;
		justify-content: center;
		align-items: center;
		list-style: none;
	}

	li {
		position: relative;
		height: 100%;
	}

	.home {
		display: flex;
		align-items: center;
		padding-left: .5rem;
	}

	nav a:not(.home) {
		display: flex;
		height: 100%;
		align-items: center;
		padding: 0 0.5rem;
		color: pink;
		font-weight: 700;
		font-size: 0.8rem;
		text-transform: uppercase;
		letter-spacing: 0.1em;
		text-decoration: none;
		/* transition: color 0.2s linear; */
		transition: background-color 400ms ease-in-out;
	}
	
	a:not(.home):hover {
		background-color: hsl(350, 100%, 17%);
	}
</style>
