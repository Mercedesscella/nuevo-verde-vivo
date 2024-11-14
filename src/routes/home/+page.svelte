<script>
    import Carousel from '../../lib/components/carousel.svelte'
	   
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
    }

</style>

<div class="Home" id="Inicio">
    <Carousel/>
    
</div>
