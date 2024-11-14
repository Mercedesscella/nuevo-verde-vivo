<script>
	import Navbar from './../lib/components/navbar.svelte';
    import '../styles/reset.css';
    import '../styles/colors.css';
    import Home from '../routes/home/+page.svelte';
    
</script>

<style>
    :root{
        font-family: "Roboto", sans-serif;
        font-size: 16px;
    }


</style>



<div class="main">
    <Home/>
</div>