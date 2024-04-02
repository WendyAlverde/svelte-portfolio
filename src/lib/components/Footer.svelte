<script>
    import {link} from "svelte-spa-router"
</script>


<footer>
    <div class="container">
        <div class="grid__item">
            <p>Wendy Alverde</p>
        </div>
        <div class="grid__item">
            <ul class="socials list-unstyled">
                <li>
                    <a href="https://www.linkedin.com/in/wendy-alverde-850761237/" target="_blank">
                        <img src="../public/icons/linkedin-in.svg" alt="">
                    </a>
                </li>
                <li>
                    <a href="https://github.com/WendyAlverde" alt="Lien vers mon profil GitHub" target="_blank">
                        <img src="../public/icons/github.svg" alt="">
                    </a>
                </li>
                <li>
                    <a href="https://www.instagram.com/chat_push/" target="_blank">
                        <img src="../public/icons/instagram.svg" alt="">
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
