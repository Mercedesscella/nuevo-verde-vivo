<script>
// @ts-nocheck

	import CarouselProducto from "./CarouselProducto.svelte";
    import MiniaturaProducto from "./MiniaturaProducto.svelte";

    export let fotoProducto="#";
    export let titulo="titulo";
    export let precio="precioUnitario";
    export let descripcion="descrpion";
    export let stock=1;
    export let cantidad=1;
    export let fotosMini=[ "/img/img1.jpg" ];

    export let img1 = "/img/img1.jpg";
    export let img2 = "/img/img2.jpg";
    export let img3 = "/img/img3.jpg"; 
    
    let images = [
      img1, 
      img2, 
      img3
    ];

    function decrementar() {
        if (cantidad > 1) {
            cantidad = parseInt(cantidad) - 1;
        }
    }
    function incrementar() {
        if (cantidad < parseInt(stock)) {
            cantidad = parseInt(cantidad) + 1;
        }
    }

</script>

<style>
    .cardProducto{
        width: 100%;
        padding: 1rem;
        gap: 2rem;
        display: flex;
        flex-direction: column;
    }
    .tituloMovil{
        font-weight: 500;
        font-size: 1.2rem;
    }
    .tituloEscritorio{
        display: none;
        font-weight: 500;
        font-size: 1.2rem;
    }
    .fotosProducto{
        display: flex;
        flex-direction: column;
        align-items: center;
        height: 20rem;
    }
    .fotoPrincipal{
        display: none;
    }
    .carrouselproducto{
        display: flex;
        flex-direction: row;
        height: 100%;
    }
    .miniaturas{
        display: none;
    }
    .foto{
        width: 100%;
        display: flex;
        justify-content: center;
        align-items: flex-end;
        overflow: hidden;
        height: 100%;
    }
    img{
        height: 100%;
        max-width: none;
    }
    .infoProducto{
        display: flex;
        flex-direction: column;
        gap: 1rem;

    }
    .infoproducto-text{
        display: flex;
        flex-direction: column;
        gap: 1rem;
    }
    .spanPrecio{
        font-weight: 400;
        font-size: 1.6rem;
    }
    .descripcion{
        font-weight: 300;
        font-size: 0.9rem;
    }
    .spanUnidades{
        font-weight: 600;
        font-size: 0.8rem;
        color: var(--plant);
    }
    
    .compra{
        display: flex;
        flex-direction: column;
        gap: 1rem;
    }
    .botones{
        display: flex;
        flex-direction: row;
        gap: 1rem;
    }
    .btnCantidad{
        width: auto;
        padding: 0.1rem;
    }
    .btnIcon{
        width: 1.6rem;
    }
    .botonesCantidad{
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: center;
        border: 2px solid var(--plantlithe);
        width: min-content;
        border-radius: 0.8rem;
        height: 2.2rem;
        
    }
    .divCantidad{
        width: 2.4rem;
        display: flex;
        align-items: center;
        justify-content: center;
        border-right: 2px solid var(--plantlithe);
        padding: 0.1rem;
        height: 100%;
        border-left: 2px solid var(--plantlithe);
        
    }
    .btnCarrito{
        background-color: var(--plantlithe);
        padding: 0.5rem 0.8rem;
        border-radius: 0.8rem;
        height: 2.2rem;
        font-size: 1rem;
        
    }
    @media (min-width: 480px){
        .fotosProducto{
            height: 20rem;
        }
    }

    @media (min-width: 640px){
        .fotosProducto{
            height: 24rem;
        }
    }
    @media(min-width: 768px){
        .cardProducto{
            flex-direction: row;
        }
        .tituloMovil{
            display: none;
        }
        .tituloEscritorio{
            display: flex;
        }
        .fotosProducto{
            width: 50%; 
            height: 16rem; 
            display: flex;
            flex-direction: row;
            gap: 1rem;  
        }
        .fotoPrincipal{
        display: flex;
        }
        .carrouselproducto{
        display: none;
        }
        .infoProducto{
            justify-content: space-between;
        }
        .botones{
            gap: 2rem;
        }
        .miniaturas{
        display: flex;
        flex-direction: column;
        justify-content: flex-start;
        height: 100%;
        gap: 1rem;
        }
        .foto{
        width: 26rem;
        
        }
    }
    @media(min-width: 1024px){
        .fotosProducto{
            height: 20rem;
            width: auto;
            gap: 1rem;
        }
    }



</style>

<div class="cardProducto">
    <h1 class="tituloMovil">{titulo}</h1>
    <div class="fotosProducto">
        <div class="miniaturas">
           
                 {#each fotosMini as foto}
                    <MiniaturaProducto fotoMiniatura={foto} />
                {/each}
        </div>

        <div class="foto"  >
            <img src={fotoProducto} alt="" class="fotoPrincipal">
            <div class="carrouselproducto">
                <CarouselProducto
                     imagesProducto= {[img1,img2,img3]}
                />
            </div>
        </div>
    </div>
    <div class="infoProducto">
        <div class="infoproducto-text">
            <h1 class="tituloEscritorio">{titulo}</h1>
            <p class="descripcion"> {descripcion}</p>
            
        </div>

        <div class="compra">
            <span class="spanPrecio">${precio}</span>
            <span class="spanUnidades">{stock} Disponible</span>
            <div class="botones">
                <div class="botonesCantidad">
                    <button class="btnCantidad" on:click={decrementar} id="menos"><img src="/img/BiDash.svg" alt="" class="btnIcon"></button>
                    <div class="divCantidad">{cantidad}</div>
                    <button class="btnCantidad" on:click={incrementar} id="mas"><img src="/img/BiPlus.svg" alt="" class="btnIcon"></button>
                </div>
                <button class= "btnCarrito">Agregar al carrito</button>
            </div>
        </div>
    </div>
    
</div>