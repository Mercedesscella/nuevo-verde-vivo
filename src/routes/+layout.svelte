<script>
    import{page}from "$app/stores";
	import Navbar from "$lib/components/Navbar.svelte";
    import Footer from "$lib/components/Footer.svelte";
    /*let currentPage = $page.url.pathname;   */
   

</script>

<Navbar/>

<main>
    <slot/>
</main>

<Footer/>
