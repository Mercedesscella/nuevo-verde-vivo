<script>
     
</script>

<style>
    .container{
    display: flex;
    flex-wrap: nowrap;
    flex-direction: row;
    gap: 0.7rem;
    justify-content: flex-start;
    scrollbar-width: none;
    overflow: auto;
    padding: 1rem 0;
    margin: 1rem 4%;

    }
    @media(min-width:1024px){
        .container{
            margin: 2rem 3%;
        }
    }
</style>

<div class="container">
    <slot><!-- optional fallback --></slot>
</div>