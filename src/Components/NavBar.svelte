<script>
    import {fly} from 'svelte/transition';
</script>
<nav>
    <div class="logo"><img src="../images/logo.svg" alt="The Compony Logo"></div>
    <button><img src="../images/icon-menu.svg" alt=""></button>
    <ul>
        <li>Features</li>
        <li>Company</li>
        <li>Careers</li>
        <li>About</li>
    </ul>
</nav>
<style>
    nav{
        padding: 1rem;
        width: 100vw;
        height: 80px;
        display: flex;
        justify-content: space-between;
        align-items: center;
        /* box-shadow: 1px 1px 20px rgba(0, 0, 0, 0.1); */
    }
    nav ul{
        display: none;
    }
    nav button{
        border: none;
        background-color: transparent;
    }
</style>