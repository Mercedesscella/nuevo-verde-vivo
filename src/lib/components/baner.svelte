<script>
    
    export let h2="h2";
    export let h1="h1";
    export let img="#";
</script>

<style>
    .baner{
        background-color: rgb(162, 238, 168);
        width: calc(100% - 2rem)
        height: 8rem;
        padding: 1rem;
        border-radius: 0.4rem;
        box-sizing: border-box;
        color: black;
        box-shadow: 0px 0px 8px 2px rgba(0,0,0,0.10);
        display: flex;
        flex-direction: row;
        justify-content: space-around;
        margin: 1rem;
        box-sizing: border-box;
    }
    .h2{
        font-size: 1rem;
        font-weight: 500;
        padding-bottom: 0.3rem;        
    }

    .h1{
        font-size: 1.3rem;
        font-weight: 400;
    }
    .foto{
        width: auto;
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

<div class="baner" >
    <div class="Texto">
        <p class="h2">{h2}</p>
        <p class="h1">{h1}</p>
    </div>
    <div class="foto"> 
        <img src="{img}" alt="">
    </div>
    

</div>