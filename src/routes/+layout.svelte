<script>
    import{page}from "$app/stores";
	import Navbar from "$lib/components/navbar.svelte";
    import Footer from "$lib/components/footer.svelte";
    /*let currentPage = $page.url.pathname;   */
   

</script>

<Navbar/>

<main>
    <slot/>
</main>

<Footer/>
