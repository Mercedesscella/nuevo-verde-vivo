<script>
    import Carousel from '../../lib/components/Carousel.svelte'
    import Baner from '$lib/components/Baner.svelte';
    import Container from '$lib/components/Container.svelte';
    import Card from '../../lib/components/Card.svelte';
	   
let images = [  
  'static/img/ofertas.jpeg',
  'static/img/plantinesProductos.jpeg',  
  'https://via.placeholder.com/600x300?text=Image+2',  
  'https://via.placeholder.com/600x300?text=Image+3',  
  'https://via.placeholder.com/600x300?text=Image+4',  
];  

</script>

<style>
     .Home{
        width: 100%;
        min-height: 50vh;
    }

</style>

<div class="Home" id="Inicio">
    <Carousel/>
    
    
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
