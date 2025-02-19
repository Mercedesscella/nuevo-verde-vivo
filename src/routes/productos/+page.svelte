<script>
	import Baner from '$lib/components/Baner.svelte';
	import CardProducto from '$lib/components/CardProducto.svelte';
    import Container from '$lib/components/Container.svelte';
    import Card from '../../lib/components/Card.svelte';
</script>

<style>
    .Productos{
        background-color: white;
        padding: 0.5rem 0;
        min-height: 50vh;
    }
    h1{
        margin: 1.5rem 5%;
        font-weight: 500;
        font-size: 1.2rem;
    }
    
    @media (min-width: 768px){
        .Productos{
            padding: 1rem 0;
        }
    }
    @media (min-width: 1024px){
        
    }
    
</style>

<div class="Productos" id="Productos">
    <h1>Productos</h1>
    <CardProducto
        fotoProducto= "/img/img2.jpg"
        titulo= "Este es el titulo del primer producto."
        precio= "2.599"
        descripcion= "descripcion general del producto nuevo vendido hoy"
        stock= "4"
        cantidad= "1"
        fotosMini={["/img/img2.jpg", "/img/img2.jpg", "/img/img2.jpg"]}
    />
    <Container> 
                  
        <Card
        titulo="Plantines"
        img="/img/lechugamanteca.jpg"
        precio="$ 1.200"
        descripcion="Plantin de tomate cherry 10cm alto"
        
        />

        <Card
        titulo="Plantines"
        img="/img/lechugamanteca.jpg"
        precio="$ 1.200"
        descripcion="Plantin de tomate cherry 10cm alto"
        />

        <Card
        titulo="Plantines"
        img="/img/lechugamanteca.jpg"
        precio="$ 1.200"
        descripcion="Plantin de tomate cherry 10cm alto"
        />

        <Card
        titulo="Plantines"
        img="/img/lechugamanteca.jpg"
        precio="$ 1.200"
        descripcion="Plantin de tomate cherry 10cm alto"
        />

    </Container>


    <Baner
        h2="Titulo mediano"
        h1="Titulo grande"
        img="/img/img3.jpg"
    />

    <Container> 
                  
        <Card
        titulo="Plantines"
        img="/img/lechugamanteca.jpg"
        precio="$ 1.200"
        descripcion="Plantin de tomate cherry 10cm alto"
        />

        <Card
        titulo="Plantines"
        img="/img/lechugamanteca.jpg"
        precio="$ 1.200"
        descripcion="Plantin de tomate cherry 10cm alto"
        />

        <Card
        titulo="Plantines"
        img="/img/lechugamanteca.jpg"
        precio="$ 1.200"
        descripcion="Plantin de tomate cherry 10cm alto"
        />

        <Card
        titulo="Plantines"
        img="/img/lechugamanteca.jpg"
        precio="$ 1.200"
        descripcion="Plantin de tomate cherry 10cm alto"
        />

    </Container>

</div>