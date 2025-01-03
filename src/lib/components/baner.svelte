<script>
    
    export let h2="h2";
    export let h1="h1";
    export let img="#";
</script>

<style>
    .baner{
        background-color: rgb(162, 238, 168);
        width: 90%;
        height: 15rem;
        border-radius: 0.4rem;
        box-sizing: border-box;
        color: black;
        box-shadow: 0px 0px 8px 2px rgba(0,0,0,0.10);
        display: flex;
        flex-direction: column ;
        margin: 1rem 5%;
        box-sizing: border-box;
    }
    .texto{
        padding:0  1rem;
        height: 50%;
    }
    .h2{
        padding-top: 1.5rem;
        font-size: 0.8rem;
        font-weight: 500;
        padding-bottom: 0.5rem;        
        margin: 0;
    }

    .h1{
        font-size: 1.4rem;
        font-weight: 400;
        margin: 0;
    }
    .foto{
        width: 100%;
        overflow: hidden;
        display: flex;
        justify-content: center;
        align-items: flex-end;
        height: 50%;
        border-radius: 0 0 0.4rem 0.4rem;
        
    }
    img{
        max-width: none;
        width: 100%;
    }
    @media(min-width: 1024px){
        .baner{
            flex-direction: row;
            margin: 3rem 3%;
            width: 94%;
        

        }
        .texto{
            height: 100%;
            width: 50%;
            padding: 1rem 0;
            margin-left: 2rem;
            box-sizing: border-box;
        }
        .h2{
            font-size: 1.2rem;
        }
        .h1{
            font-size: 1.8rem;
        }
        .foto{
            height: 100%;
            width: 50%;
            border-radius: 0 0.4rem 0.4rem 0;
        }
    }
</style>

<div class="baner" >
    <div class="texto">
        <p class="h2">{h2}</p>
        <p class="h1">{h1}</p>
    </div>
    <div class="foto"> 
        <img src="{img}" alt="">
    </div>
    

</div>