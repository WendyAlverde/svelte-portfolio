<script>
    import {link} from "svelte-spa-router"
    // Import pictures
    import ocook from "../../assets/icons/site/portfolio/ocook-logo-blue.webp"
</script>

<main>
    <h1>Portfolio</h1>
    <p>La programmation est la clé qui ouvre les portes du renouveau technologique, où l'imagination devient réalité et où les possibilités deviennent infinies.</p>

    <section id="portfolio">
        <section id="web">
            <h2>Développement web</h2>
            <article>
                <img src={ocook} loading="lazy" alt="Logo du projet O'Cook"> <!--Mettre des images en paysage-->
                <a href="/ocook" use:link>O'Cook</a>
                <p>O'Cook est un blog de gastronomie et de critiques de restaurants, écrit par Alice Ocklecook. C'est un projet de groupe réalisé sous la méthode SCRUM en fin de formation avec l'école O'Clock.</p>
            </article>
            <article>
                <img src="" loading="lazy" alt="">
                <a href="/">Yoga</a>
                <p>Un site administratif pour une gérante d'association de cours de yoga.</p>
            </article>
        </section>
        <section id="games" >
            <h2>Développement jeux vidéo</h2>
            <article>
                <img src="" loading="lazy" alt="">
                <a href="/">Le monde des rêves</a>
                <p>Un jeu de plateforme créer sur Contruct3.</p>
            </article>
        </section>
    </section>
</main>

<style lang="scss">
    #portfolio img{
        width: 5rem;
    }
    
    a {
        color:black;
    }
</style>