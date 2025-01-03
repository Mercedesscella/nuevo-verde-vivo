<script>
	import { _experimentalBidi } from "@playwright/test";

    export let FotoProducto="#";
    export let titulo="titulo";
    export let precio="precioUnitario";
    export let descripcion="descrpion";
    export let stock="1";
    export let cantidad="00";
</script>
<style>

</style>
<div class="cardProducto">
    <div class="fotosProducto">
        <div class="miniaturas"></div>
        <div class="foto">{FotoProducto}</div>
    </div>
    <div class="infoProducto">
        <h1>{titulo}</h1>
        <span>${precio}</span>
        <p> {descripcion}</p>

        <div class="compra">
            <span>{stock} Unidades</span>
            <div class="botones">
                <div class="cantidad">
                    <button ><img src="/img/BiDash.svg" alt=""></button>
                    <span>{cantidad}</span>
                    <button><img src="/img/BiPlus.svg" alt=""></button>
                </div>
                <button class= "carrito">Agregar al carrito</button>
            </div>
        </div>
    </div>
    
</div>