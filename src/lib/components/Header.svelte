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
    <a class="header-logo" href="/" use:link>Wendy Alverde</a>

    <nav class="header-nav">
        <ul class="header-nav-list">
            <li><a href="/" title="Accueil" use:link>Accueil</a></li>
            <li><a href="/portfolio" title="Portfolio" use:link>Portfolio</a></li>
            <li><a href="/contact" title="Contact" use:link>Contact</a></li>
            <li><a href="/cv" title="Mon CV" use:link>Mon CV</a></li>
        </ul>
    </nav>
    
    <section class="header-right">
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
        <!-- Mobile -->
        {#if menuOpen}
            <button class="mobile" on:click="{closeMenu}" aria-hidden="false">
                <nav class="mobile-nav" >
                    <ul class="mobile-nav-list">
                        <li><a href="/" title="Accueil" use:link>Accueil</a></li>
                        <li><a href="/portfolio" title="Portfolio" use:link>Portfolio</a></li>
                        <li><a href="/contact" title="Contact" use:link>Contact</a></li>
                        <li><a href="/cv" title="Mon CV" use:link>Mon CV</a></li>
                    </ul>
                </nav>
            </button>
        {/if}
        <!-- Mobile -->

    </section>
    
</header>

<style lang="scss">
    .header { 
        background: var(--background-entete);
        border-radius: 0.3rem;
        box-shadow: 0 0 5px #548072; 
        position: sticky;
        top: 0;
        display: flex;
        align-items: flex-end;
        justify-content: space-between;
        padding: 0.5rem 1rem;

        @media (min-width: 770px) { /*PC*/
            padding: 0.8rem 2rem;
        }

        &-logo {
            font-family: 'Playfair Display', serif;
            color: var(--color-text);
            font-size: 1.2rem;

            &:hover {
                color: var(--color-passagesouris);
            }

            @media (min-width: 710px) and (max-width: 769px) { /*Tablette*/
                font-size: 1.5rem;
                letter-spacing: 1px;
            }

            @media (min-width: 770px) { /*PC*/
                font-size: 2rem;
                letter-spacing: 2px;
            }

        }

        &-nav {
            display: none;
            
            @media (min-width: 710px) and (max-width: 991px) { /*Tablette*/
                display: flex;

                &-list {
                    display: flex;
                    gap: 1rem;

                    a {
                        color: var(--color-text);
                        font-size: 1.5rem;

                        &:hover {
                            color: var(--color-passagesouris);
                        }
                    }
                }
            }
            @media (min-width: 991px) { /*PC*/
                display: flex;

                &-list {
                    display: flex;
                    gap: 2rem;

                    a {
                        color: var(--color-text);
                        font-size: 2rem;

                        &:hover {
                            color: var(--color-passagesouris);
                        }
                    }
                }
            }
        }

        &-right {
            display: flex;
            align-items: flex-end;
            gap: 1rem;

            .socials {
                display: flex;

                &__icon {
                    width: 1.2rem;
                    height: 1.2rem;

                    @media (min-width: 710px) and (max-width: 991px) { /*Tablette*/
                        width: 1.5rem;
                        height: 1.5rem;
                    }
                    @media (min-width: 991px) { /*PC*/
                        width: 2rem;
                        height: 2rem;
                    }
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

                @media (min-width: 710px) {
                    display: none;
                }

                .burger__bar {
                    display: block;
                    width: 1.3rem;
                    height: 0.2rem;
                    background-color: var(--color-text);
                    position: absolute;
                    transition: transform 0.3s ease, opacity 0.3s ease;
                    z-index: 3;

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

            .mobile {
                position: fixed;
                top: 0;
                left: 0;
                width: 100%;
                height: 100%;
                background: rgba(0, 0, 0, 0.5); /* Fond transparent sombre */
                display: flex;
                justify-content: flex-end; /* Aligner le menu à droite */
                z-index: 2; /* Au-dessus de tout */

                &-nav {
                    width: 50%;
                    max-width: 20rem;
                    background: var(--background-entete);
                    height: auto; /* Hauteur selon le contenu */
                    padding: 1rem;
                    position: relative;
                    display: flex;
                    flex-direction: column;
                    border: 0.2rem solid var(--color-text);
                    border-radius: 3%;

                    &-list {
                        display: flex;
                        flex-direction: column;
                        gap: 1rem;
                        margin: 1rem 0;

                        li {
                            padding: 0.5rem;

                            a {
                                color: var(--color-text);
                                text-decoration: none;
                                font-size: 1.5rem;

                                &:hover {
                                    color: var(--color-passagesouris);
                                }
                            }
                        }
                    }
                }
            }
        }
    }

    // @media (min-width: 770px) { /*PC*/

    //     .header__nav {
    //         display: block;

    //         & .header__menu { 
    //             display: flex;
    //             flex-direction: row;
    //             justify-content: space-around;
    //             padding-top: 1rem;
    //         }
    //     }
    // }
</style>