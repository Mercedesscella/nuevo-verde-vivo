<script>
	import Footer from './footer.svelte';

</script>

<style>
    .footer{
        background-color: var(--plantlithe);
        width: 100%;
        height: auto;
    }
    ul{
        display: flex;
        flex-direction: column;
        padding: 0.4rem 0;
    }
    li{
        font-size: 0.8rem;
        color: #201f1f;
        font-weight: 400;
        padding: 0.4rem 0;
        text-align: center;
        line-height: 1rem;
    }

    @media(min-width: 768px){
        ul{
            flex-direction: row;
            justify-content: space-around;
        }
        li{
            font-size: 1rem;
            line-height: 1.5rem;
        }
        .li2{
            padding-top: 2rem;
            
        }
        .footer{
        padding: 1.5rem 0;
        }   
    }
</style>


<div class="footer">
    <ul>
        <li><a href="mailto:verdevivo@gmial">verdevivo@gmial</a></li>
        <li class="li2">Horario de atencion: <br> De 9:00 a 18:00 de lunes a sabado</li>
        <li><a href="/Sobrenosotros">Sobre nosotros</a></li>
    </ul>

</div>