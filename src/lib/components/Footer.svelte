<script>
    import {link} from "svelte-spa-router";
    // import pictures
    import logoWa from "../../assets/logo/WA.svg";
    import linkedin from "../../assets/site/socials/linkedin.svg";
    import github from "../../assets/site/socials/github.svg";
    import instagram from "../../assets/site/socials/instagram.svg";
</script>

<footer>
    <a class="logo" href="/" use:link aria-label="Retour à l'accueil">
        <img class="logoWa" src={logoWa} loading="lazy" alt="Logo du site de Wendy Alverde">
    </a>
    <div class="item">
        <ul class="socials list-unstyled">
            <li>
                <a href="https://www.linkedin.com/in/wendy-alverde-850761237/" target="_blank" alt="Lien vers mon profil LinkedIn">
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
    <a class="red" href="/legal-notices" use:link>Mentions légales</a>
    <div class="item">
        <p>Copyright 2025 Wendy Alverde - Tous droits réservés.</p>
    </div>
</footer>

<style lang="scss">
    footer { 
        background: var(--background-entete);
        border-bottom: 1px solid #eee;
        border-radius: 0.2rem;
        box-shadow: 0 0 5px #548072; 
        text-align: center;

        .logoWa {
            margin: 0.3rem 0;
            width: 2.8rem;
            height: 1.5rem;

            @media (min-width: 710px) and (max-width: 769px) { /*Tablette*/
                width: 4.5rem;
                height: 3rem;
            }
            @media (min-width: 770px) { /*PC*/
                width: 5.5rem;
                height: 4rem;
            }
        }

        .socials {
            display: flex;
            flex-direction: row;
            justify-content: center;
        }
    }

    
</style>