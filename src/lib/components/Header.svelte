<script>
    import {link} from "svelte-spa-router";
    import { onMount } from 'svelte';
    // import pictures
    import linkedin from "../../assets/icons/site/socials/linkedin.svg";
    import github from "../../assets/icons/site/socials/github.svg";
    import instagram from "../../assets/icons/site/socials/instagram.svg";

    // Menu burger
    // État pour contrôler l'ouverture du menu
    let menuOpen = false;

    // Fonction pour ouvrir/fermer le menu
    function toggleMenu() {
        menuOpen = !menuOpen;
    }

    // Fonction pour fermer le menu
    function closeMenu() {
        menuOpen = false;
    }
</script>

<header class="header">
    <a class="header__logo" href="/" use:link>Wendy Alverde</a>

    {#if menuOpen}
        <button class="menu-overlay" on:click="{closeMenu}" aria-hidden="false">
            <nav class="menu" >
                <ul class="header__menu list-unstyled">
                    <li><a href="/" title="Accueil" use:link>Accueil</a></li>
                    <li><a href="/portfolio" title="Portfolio" use:link>Portfolio</a></li>
                    <li><a href="/contact" title="Contact" use:link>Contact</a></li>
                    <li><a href="/cv" title="Mon CV" use:link>Mon CV</a></li>
                </ul>
            </nav>
        </button>
    {/if}

    <ul class="socials">
        <li>
            <a href="https://www.linkedin.com/in/wendy-alverde-850761237/" target="_blank">
                <img class="socials__icon" src={linkedin} alt="Lien vers mon profil LinkedIn">
            </a>
        </li>
        <li>
            <a href="https://github.com/WendyAlverde" target="_blank">
                <img class="socials__icon" src={github} alt="Lien vers mon profil GitHub">
            </a>
        </li>
        <li>
            <a href="https://www.instagram.com/chat_push/" target="_blank">
                <img class="socials__icon" src={instagram} alt="Lien vers mon profil Instagram">
            </a>
        </li>
    </ul>

    <button class="burger" aria-pressed={menuOpen} aria-label={menuOpen ? "Fermer le menu" : "Ouvrir le menu"} on:click={toggleMenu}>
        <em class="burger__bar"></em>
    </button>
</header>

<style lang="scss">
    .header { 
        background: var(--background-entete);
        border-bottom: 1px solid #eee;
        border-radius: 0.3rem;
        box-shadow: 0 0 5px #548072; 
        position: sticky;
        top: 0;
        display: flex;
        align-items: center;
        padding: 0.5rem 1rem;

        &__logo {
            font-family: 'Playfair Display', serif;
            letter-spacing: 1px;
            color: var(--color-text);

            &:hover {
                color: var(--color-passagesouris);
            }
        }

        .menu-overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.5); /* Fond transparent sombre */
            display: flex;
            justify-content: flex-end; /* Aligner le menu à droite */
            z-index: 2; /* Au-dessus de tout */

            .menu {
                width: 80%;
                max-width: 20rem;
                background: var(--background-entete);
                height: auto; /* Hauteur selon le contenu */
                box-shadow: -2px 0 5px rgba(0, 0, 0, 0.2);
                padding: 1rem;
                position: relative;
                display: flex;
                flex-direction: column;
                align-items: flex-start;

                &__close {
                    position: absolute;
                    top: 1rem;
                    right: 1rem;
                    background: none;
                    border: none;
                    font-size: 2rem;
                    cursor: pointer;
                    color: var(--color-text);
                }

                .header__menu {
                    display: flex;
                    flex-direction: column;
                    gap: 1rem;

                    a {
                        color: var(--color-text);
                        text-decoration: none;

                        &:hover {
                            color: var(--color-passagesouris);
                        }
                    }
                }
            }
        }


        &__nav {
            display: none;
            overflow: hidden;
            background: var(--background-entete);
            transition: all 0.4s ease-out;

            & .header__menu {
                margin-top: 0.6rem;
            }
        }
    }

    .socials {
        display: flex;

        &__icon {
            width: 1.5rem;
            height: 1.5rem;
        }
    }

    .burger {
        background: none;
        border: none;
        width: 2.1rem;
        height: 2.1rem;
        position: relative;
        cursor: pointer;
        display: flex;
        justify-content: center;
        align-items: center;

        .burger__bar {
            display: block;
            width: 1.3rem;
            height: 0.2rem;
            background-color: var(--color-text);
            position: absolute;
            transition: transform 0.3s ease, opacity 0.3s ease;
            z-index: 2;

            &::before,
            &::after {
                display: block;
                content: '';
                width: 1.3rem;
                height: 0.2rem;
                background-color: var(--color-text);
                position: absolute;
                transition: transform 0.3s ease, opacity 0.3s ease;
            }

            &::before {
                transform: translateY(-0.5rem);
            }

            &::after {
                transform: translateY(0.5rem);
            }
        }
        // Quand le menu est ouvert
        &[aria-pressed="true"] .burger__bar {
            background-color: transparent;

            &::before {
                transform: rotate(45deg);
            }

            &::after {
                transform: rotate(-45deg);
            }
        }
    }

    /* Responsive */
    @media screen and (min-width: 426px) and (max-width: 768px) { /*Tablette*/
        .header__logo {
            font-size: 1.5rem;
            letter-spacing: 1px;
        }

        .header__nav {
            display: block;
        }

        .burger {
            display: none;
        }
        .menu-overlay {
            display: none;
        }
    }

    @media screen and (min-width: 769px) { /*PC*/
        .header__logo {
            font-size: 2rem;
            letter-spacing: 2px;
        }

        .header__nav {
            display: block;

            & .header__menu {
                display: flex;
                flex-direction: row;
                justify-content: space-around;
                padding-top: 1rem;
            }
        }

        .burger {
            display: none;
        }
    }
</style>