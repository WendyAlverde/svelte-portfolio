<script>
    import {link} from "svelte-spa-router"
</script>

<header role="banner">
    <div class="container">
        <div class="logo">Wendy Alverde</div>
        <nav role="navigation">
            <ul class="menu list-unstyled">
                <li><a href="/" title="Cliquer pour aller sur la page d'accueil" use:link>Accueil</a></li>
                <li><a href="/portfolio" title="Cliquer pour aller sur la page portfolio" use:link>Portfolio</a></li>
                <li><a href="/contact" title="Cliquer pour aller sur la page contact" use:link>Contact</a></li>
                <li><a href="/cv" title="Cliquer pour aller sur la page de mon curriculum vitae" use:link>Mon CV</a></li>
            </ul>
        </nav>
        <div class="right">
            <ul class="socials">
                <li>
                    <a href="https://www.linkedin.com/in/wendy-alverde-850761237/" alt="Lien vers mon profil LinkedIn" target="_blank">
                        <img class="icon" src="../public/icons/linkedin-in.svg" alt="Logo amenant sur le profil LinkedIn de Wendy Alverde">
                    </a>
                </li>
                <li>
                    <a href="https://github.com/WendyAlverde" target="_blank" alt="Lien vers mon profil GitHub">
                        <img class="icon" src="../public/icons/github.svg" alt="Logo amenant sur le profil GitHub de Wendy Alverde">
                    </a>
                </li>
                <li>
                    <a href="https://www.instagram.com/chat_push/" target="_blank" alt="Lien vers mon profil LinkedIn">
                        <img class="icon" src="../public/icons/instagram.svg" alt="Logo amenant sur le profil Instagram de Wendy Alverde">
                    </a>
                </li>
            </ul>
            <button role="button" aria-pressed="false" class="burger"><em class="bar"></em></button>
        </div>
    </div>
    <div class="banniere">
        <p>SITE EN CONSTRUCTION</p>
    </div>
</header>
