<script>
	import Navbar from '../lib/components/Navbar.svelte';
    import '../styles/reset.css';
    import '../styles/colors.css';
    import Home from './Home/+page.svelte';
    
</script>

<style>
    :root{
        font-family: "Roboto", sans-serif;
        font-size: 16px;
    }
    .main{
        display: flex;
        flex-direction: column;
        justify-content: space-between;
    }
   

</style>



<div class="main">
    <Home/>
</div>