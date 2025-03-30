<script lang="ts">
    import Page from './+page.svelte'
    import {} from './style/globa.css'
</script>

<div>
    <header>
        <nav>
            <ul>
                <li><a href="#tryby">Nasze Tryby</a></li>
                <li><a href="#team">Nasz Team</a></li>
                <li><a href="#map">Mapa SMP</a></li>
                <li><a href="https://vishop.pl/shop/204/server/120" target="_blank">Sklep</a></li>
                <li><a href="#fqa">FAQ</a></li>
            </ul>
        </nav>
    </header>

    <Page></Page>

    <footer>
        <div class="footer-content">
            <p>Jakiś tekst w stopce. Możesz dodać Mateuszku jakieś linki, informacje o prawach autorskich, itp.</p>
            <div class="footer-links">
                <a href="#">Polityka prywatności</a> 
                <a href="#">Warunki użytkowania</a>
            </div>
            <p>PL - Serwer StonksCraft.pl nie jest w żaden sposób powiązany z firmą Mojang lub Microsoft.</p>
            <p>EN - StonksCraft.pl server is not associated with Mojang or Microsoft in any way.</p>
        </div>
    </footer>
</div>

<style>
    /* Styl headera */
    header {
        height: 70px;
        width: 100%;
        background-color: #333;
        display: flex;
        align-items: center;
        justify-content: center;
    }

    nav ul {
        display: flex;
        gap: 30px;
        margin: 0;
        padding: 0;
        list-style: none;
    }

    nav ul li {
        margin: 0;
    }

    nav ul li a {
        color: white;
        text-decoration: none;
        font-size: 16px;
        font-weight: 500;
        transition: color 0.3s ease;
    }

    nav ul li a:hover {
        color: #ff8c00;
    }

    /* Styl footer */
    footer {
        height: 200px;
        width: 100%;
        background-color: #f0f0f0;
        display: flex;
        justify-content: center;
        align-items: center;
        padding: 20px;
        box-sizing: border-box;
    }

    .footer-content {
        text-align: center;
        max-width: 1200px;
        width: 100%;
    }

    .footer-content p {
        font-size: 14px;
        color: #333;
        margin-bottom: 10px;
    }

    .footer-links {
        font-size: 14px;
        color: #555;
        margin-bottom: 20px;
    }

    .footer-links a {
        text-decoration: none;
        color: #555;
        transition: color 0.3s ease;
    }

    .footer-links a:hover {
        color: #ff8c00;
    }
</style>
