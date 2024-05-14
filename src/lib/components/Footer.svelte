<script>
    import {link} from "svelte-spa-router"
    import linkedin from "../../assets/icons/site/linkedin.svg"
    import github from "../../assets/icons/site/github.svg"
    import instagram from "../../assets/icons/site/instagram.svg"
</script>


<footer>
    <div class="container">
        <div class="grid__item">
            <p>Wendy Alverde</p>
        </div>
        <div class="grid__item">
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
        <div class="grid__item">
            <p>Copyright 2024 Wendy Alverde - Tous droits réservés.</p>
        </div>
    </div>
</footer>
