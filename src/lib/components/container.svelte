<script>
     
</script>

<style>
    .container{
    display: flex;
    flex-wrap: nowrap;
    flex-direction: row;
    gap: 1.5rem;
    justify-content: flex-start;
    scrollbar-width: none;
    overflow: auto;
    padding: 1rem 0;

    }
</style>

<div class="container">
    <slot><!-- optional fallback --></slot>
</div>