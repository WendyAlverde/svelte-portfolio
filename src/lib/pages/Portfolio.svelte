<script>
    import {link} from "svelte-spa-router"
    // Import pictures
    import ocook from "../../assets/site/portfolio/ocook-logo-blue.webp"
</script>

<main role="main">
    <h1>Portfolio</h1>
    <p>La programmation est la clé qui ouvre les portes du renouveau technologique, où l'imagination devient réalité et où les possibilités deviennent infinies.</p>
    <!-- <p>"Le développement est un voyage constant où chaque projet m'apporte de nouvelles connaissances et perspectives."</p> -->

    <section id="portfolio">
        <article>
            <img src={ocook} loading="lazy" alt="Logo du projet O'Cook"> <!--Mettre des images en paysage-->
            <a href="/ocook" use:link>O'Cook</a>
            <p>O'Cook est un blog de gastronomie et de critiques de restaurants, écrit par Alice Ocklecook. C'est un projet de groupe réalisé sous la méthode SCRUM en fin de formation avec l'école O'Clock.</p>
        </article>
        <article>
            <img src="" loading="lazy" alt="">
            <a href="#">A venir</a>
            <p></p>
        </article>
        <article>
            <img src="" loading="lazy" alt="">
            <a href="#">A venir</a>
            <p></p>
        </article>
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