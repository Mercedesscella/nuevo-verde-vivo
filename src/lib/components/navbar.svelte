<script>
    import { onMount } from 'svelte';

    let showMenu = false;
    let isMobile = true;

    function closeMenu() {
        if (isMobile) {
            showMenu = false;
        }
    }

    function toggleMenu() {
        if (isMobile) {
            showMenu = !showMenu;
        }
    }

    function handleResize() {
        if (window.innerWidth >= 768) {
            isMobile = false;
            showMenu = true;
        } else {
            isMobile = true;
            showMenu = false;
        }
    }

    onMount(() => {
        handleResize();
        window.addEventListener('resize', handleResize);
        return () => window.removeEventListener('resize', handleResize);
    });

    function smoothScroll(event) {
        event.preventDefault();
        const targetId = event.currentTarget.getAttribute("href").substring(1);
        const targetElement = document.getElementById(targetId);
        targetElement.scrollIntoView({ behavior: "smooth" });
    }
</script>


<style>
    .Navbar {
        width: 100%;
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: space-between;
        background-color: var(--newGrowph);
        padding: 0.5rem 5%;
    }
    .logo {
        font-size: 2rem;
        color: var(--black);
        font-family: "Dating";
        font-weight: 800;
    }
    .btn-menu {
        height: 1.5rem;
        cursor: pointer;
    }
    .menu {
        width: 100%;
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        align-items: center;
        
    }
    .menu-links {
        display: flex;
        flex-direction: column;
        align-items: flex-end;
        padding: 0.4rem 0;
        overflow: hidden;
        position: absolute;
        width: 100%;
        background-color: var(--newGrowph);
        padding-right: 5%;
        top: 3rem;
        z-index: 3;
        left: 0;
    }
    li {
        font-size: 1.1rem;
        padding: 0.6rem 0;
        color: var(--davys-gray);
        cursor: pointer;
        transition: all 0.3s ease;
    }
    .link {
        text-decoration: none;
        color: inherit;
        font-weight: 300;
        font-size: 1rem;
    }

    .divBuscador{
        background-color: white;
        display: flex;
        flex-direction: row;
        align-items: center;
        border-radius: 0.2rem;
        width: auto;
        height: 2.4rem;
        margin: 0 5%;
    }

    .lupa{
        width: 1.8rem;
        margin: 0.1rem 0.2rem;
    }
    .buscador{
        width: 100%;
        border: none;
        font-size: 1rem;
        font-weight: 300;
        color: #666666;
        margin: 0 0.2rem;
        background-color: transparent;

    }

    .iconocarrito{
        width: 1.6rem;
    }
    .divcarrito{
        padding-left: 5%;
    }
    
    .carritoescritorio{
        display: none;
    }
    

    @media (min-width: 768px) {
        .Navbar {
            padding: 1rem 5%;
            flex-direction: column;
            gap: 1rem;
        }
        
        .logo {
            font-size: 2.4rem;
        }
        .divBuscador{
            width: 100%;
        }
        .buscador{
            font-size: 1rem;
        }
        .menu {
            padding: 0;
            width: 100%;
        }
        .navlinks{
            display: flex;
            flex-direction: row;
            width: 100%;
            justify-content: space-between;
            height: 2rem;
        }
        .menu-links {
            flex-direction: row;
            position: static;
            padding: 0rem 0 0;
            background-color: transparent;
            padding-right: 0;
            z-index: 1;
            display: flex;
            align-items: center;
            justify-content: center;
            width: auto;
        }
        .link {
            padding: 0 0.1rem;
            margin: 0rem 1rem;
            
        }
        
        .btn-menu {
            display: none;
        }
        .divcarrito{
        display: none;
        
        }

        .ingresarmobil{
            display: none;
        }

        .carritoescritorio{
        display: flex;
        flex-direction: row;
        align-items: center;
        }

    }
    @media (min-width: 1024px) {
        .Navbar {
            padding: 1.7rem 5%;
            gap: 1.7rem;
        }
        .link{
            font-size: 1.3rem;
        }
        .divBuscador{
            height: 3.4rem;
            padding: 0 2rem;
        }
    }
    
</style>

<nav class="Navbar">
    <div class="menu">
        <p class="logo">logo</p>
        <div class="divBuscador">
            <input type="text" class="buscador"> 
            <img src="/img/buscador.svg" alt=""  class="lupa">
        </div>
        <img src="/img/IconoMenu.svg" alt="menu" class="btn-menu" on:click={toggleMenu}>
    </div>

    <div class="navlinks">
        {#if showMenu || !isMobile}
            <ul class="menu-links">
                <li><a href="/" class="link" on:click={closeMenu}>Inicio</a></li>
                <li><a href="/Servicios"  class="link" on:click={closeMenu}>Servicios</a></li>
                <li><a href="/Productos"  class="link" on:click={closeMenu}>Productos</a></li>
                <li><a href="/GuiadeHuerta"  class="link" on:click={closeMenu}>Guia de huerta</a></li>
                <li class="ingresarmobil"><a href="#ingresar"  class="link" on:click={closeMenu}>Ingresar</a></li>
            </ul>
        
        {/if}
        
        <ul class="carritoescritorio">
            <li><a href="#ingresar" on:click={smoothScroll} class="link">Ingresar</a></li>
            <li><a href="#carrito" on:click={smoothScroll} class="link"><img class="iconocarrito" src="/img/carrito.svg" alt=""></a></li>
        </ul>
    </div>
        
    <div class=divcarrito>
        <ul>
            <li><a href="#carrito" on:click={smoothScroll} class="link"><img class="iconocarrito" src="/img/carrito.svg" alt=""></a></li>
        </ul>
    </div>
</nav>