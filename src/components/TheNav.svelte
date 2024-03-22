<script>
	import { page } from '$app/stores';
</script>
<nav>
	<ul>

		
		<li aria-current={$page.url.pathname === '/' ? 'page' : undefined}>
			<a href="/">Home</a>
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
		justify-content: center;
		--background: rgba(255, 255, 255, 0.7);
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

	

	nav a {
		display: flex;
		height: 100%;
		align-items: center;
		padding: 0 0.5rem;
		color: var(--color-text);
		font-weight: 700;
		font-size: 0.8rem;
		text-transform: uppercase;
		letter-spacing: 0.1em;
		text-decoration: none;
		transition: color 0.2s linear;
	}

	a:hover {
		color: pink;
	}
</style>
