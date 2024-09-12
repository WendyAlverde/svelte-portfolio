<script>
    import {link} from "svelte-spa-router"
    // import pictures
    import linkedin from "../../assets/icons/site/socials/linkedin.svg"
    import github from "../../assets/icons/site/socials/github.svg"
    import instagram from "../../assets/icons/site/socials/instagram.svg"
</script>

<footer>
    <div class="container">
        <div class="item">
            <p>Wendy Alverde</p>
        </div>
        <div class="item">
            <ul class="socials list-unstyled">
                <li>
                    <a href="https://www.linkedin.com/in/wendy-alverde-850761237/" alt="Lien vers mon profil LinkedIn" target="_blank">
                        <img class="icon" src={linkedin} alt="Logo amenant sur le profil LinkedIn de Wendy Alverde">
                    </a>
                </li>
                <li>
                    <a href="https://github.com/WendyAlverde" target="_blank" alt="Lien vers mon profil GitHub">
                        <img class="icon" src={github} alt="Logo amenant sur le profil GitHub de Wendy Alverde">
                    </a>
                </li>
                <li>
                    <a href="https://www.instagram.com/chat_push/" target="_blank" alt="Lien vers mon profil LinkedIn">
                        <img class="icon" src={instagram} alt="Logo amenant sur le profil Instagram de Wendy Alverde">
                    </a>
                </li>
            </ul>
        </div>
        <a href="/legal-notices" use:link>Mentions légales</a>
        <div class="item">
            <p>Copyright 2024 Wendy Alverde - Tous droits réservés.</p>
        </div>
    </div>
</footer>

<style lang="scss">
    footer { 
        background: var(--background-entete);
        border-bottom: 1px solid #eee;
        border-radius: 0.2rem;
        box-shadow: 0 0 5px #548072; 
        margin-bottom: 1rem;
        text-align: center;
    }

    .socials {
        display: flex;
        flex-direction: row;
        justify-content: center;
    }
</style>