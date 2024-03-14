<script>
    import {link} from "svelte-spa-router"
</script>

<header class="header">
    <div class="container d-flex">
        <div class="logo">Wendy Alverde</div>
        <nav class="navbar">
            <ul class="menu list-unstyled">
                <li><a href="/"use:link>Accueil</a></li>
                <li><a href="#about" use:link>À propos</a></li>
                <li><a href="#skills" use:link>Mes compétences</a></li>
                <li><a href="/portfolio" use:link>Portfolio</a></li>
                <li><a href="/contact" use:link>Contacts</a></li>
                <li><a href="/cv" use:link>Mon CV</a></li>
            </ul>
        </nav>
        <div class="right">
            <ul class="socials list-unstyled">
                <li>
                    <a href="https://www.linkedin.com/in/wendy-alverde-850761237/" target="_blank">
                        <svg></svg>
                    </a>
                </li>
                <li>
                    <a href="https://www.instagram.com/chat_push/" target="_blank">
                        <svg></svg>
                    </a>
                </li>
            </ul>
            <button class="burger"><span class="bar"></span></button>
        </div>
    </div>
    <section class="banniere">
        <div class="container d-flex">
            <div class="text">
                <nav class="navbar">
                    <p>SITE EN CONSTRUCTION</p>
                </nav>
            </div>
        </div>
    </section>
</header>
