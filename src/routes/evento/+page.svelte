<script>
    import { page } from '$app/stores';
    import TheMain from '../../components/TheMain.svelte';
    import todosEventos from '../../mock/fichero-dias.json'
    // console.log(eventos[page.url.searchParams.get('dia')]);

    const dia = $page.url.searchParams.get('dia')
    const cod = $page.url.searchParams.get('codigo-evento')


    const { eventos = [] } = todosEventos[dia] // desestructuracion
  
    const [evento] = eventos.filter(
        function (item) {
            return item.id === cod
        }
    )

   
 
</script>


    <h1>        
        {evento.titulo}
    </h1>
    <p>HORA: {evento.hora}</p>
    <p>LUGAR: {evento.lugar}</p>
    <p>ACTO: {evento.descripcion}</p>

