<script>
 	import { page } from '$app/stores';
    import dias from '../mock/fichero-dias.json';  // dias es una variable que me guarda el contenido del archivo fichero-dias que está en formato json y me lo convierte a objeto
    import TheMain from './TheMain.svelte';
   
    
</script>

<TheMain>

    <h1>LOS EVENTOS GRATUITOS QUE TENEMOS PARA HOY SON:</h1>
    <nav>
        {#if dias.hasOwnProperty($page.url.pathname)}
        {#each dias[$page.url.pathname]?.eventos as evento}
            
        <a href="/evento/?codigo-evento={evento.id}&dia={$page.url.pathname}">
            <img src="/images/{evento.imagen}" width="600"  height=208 alt={evento.titulo} title={evento.titulo}>
            <strong>{evento.titulo}</strong>
            
        </a>
        {/each}
        {/if}

    </nav>
 

</TheMain>
    


<style>
    

* {
    box-sizing: border-box;
}

h1 {
    text-align: center;
}

img{
	border-radius:20px;
	border:2px solid black;
    object-fit: cover;
    width: fit-content;
	
}

nav{
	

    display: grid;
    grid-template-columns: repeat(3, 1fr);
    /* grid-template-columns: repeat(auto-fill, minmax(300px, 1fr)); */
    gap: .5rem;
    padding: .5rem;
}

@media (max-width: 400px) {
    nav {

        grid-template-columns: repeat(2, 1fr);
    }
}
</style>