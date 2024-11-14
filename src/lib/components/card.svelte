<script>
    export let titulo="titulo";
    export let precio="precio";
    export let descripcion="descripcion";
    export let img="#";
</script>

<style>
    .card{
        background-color: white;
        width: 8rem;
        height: 12rem;
        padding: 1rem;
        border-radius: 0.4rem;
        color: black;
        box-shadow: 0px 0px 8px 2px rgba(0,0,0,0.10);
        display: flex;
        flex-direction: column;
    }
    .titulo{
        font-size: 0.8rem;
        font-weight: 500;
        padding-bottom: 0.3rem;
        
    }
    .precio{
        font-size: 1rem;
        font-weight: 400;
        padding: 0.3rem 0;
    }
    .descripcion{
        font-size: 0.65rem;
        font-weight: 400;
    }
    .foto{
        width: 100%;
        height: 6rem;
        overflow: hidden;
        display: flex;
        justify-content: center;
        align-items: flex-end;
    }
    img{
        max-width: none;
        height: 100%;
    }
</style>

<div class="card" id="Sobrenosotros">
    <h1 class="titulo">{titulo} </h1>
    <div class="foto"> 
        <img src="{img}" alt="">
    </div>
    <div class="info">
        <p class="precio">{precio}</p>
        <p class="descripcion">{descripcion}</p>
    </div>

</div>