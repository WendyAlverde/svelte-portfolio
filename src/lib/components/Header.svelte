<script>
    import {link} from "svelte-spa-router";
    import { onMount } from 'svelte';

    // import pictures
    import logoWa from "../../assets/logo/WA.svg";
    import linkedin from "../../assets/site/socials/linkedin.svg";
    import github from "../../assets/site/socials/github.svg";
    import instagram from "../../assets/site/socials/instagram.svg";

    // Menu burger
    // État pour contrôler l'ouverture du menu
    let menuOpen = false;

    // Fonction pour ouvrir/fermer le menu
    function toggleMenu() {
        menuOpen = !menuOpen;
        // Menu burger ouvert, bloquer le défilement de la page
        document.body.classList.toggle('menu-open', menuOpen);
    }

    // Fonction pour fermer le menu
    function closeMenu() {
        menuOpen = false;
        // Menu burger ouvert, bloquer le défilement de la page
        document.body.classList.remove('menu-open');
    }

    let firstFocusableElement;
    let lastFocusableElement;

    onMount(() => {
        //  Gère les interactions clavier dans le menu
        const handleKeyPress = (event) => {
            if (!menuOpen) return;
            // Ferme le menu si la touche "Échap" est pressée
            if (event.key === "Escape") {
                closeMenu();
            }
            // Gère la navigation au clavier avec la touche "Tab" pour le focus
            if (event.key === "Tab") {
                // Sélectionne tous les éléments pouvant être focalisés dans le menu (liens et bouton)
                const focusableElements = document.querySelectorAll(
                    ".mobile-nav-list a, .mobile"
                );
                // Identifie le premier et le dernier élément du menu
                firstFocusableElement = focusableElements[0];
                lastFocusableElement = focusableElements[focusableElements.length - 1];
                // Si "Shift + Tab" est pressé et qu'on est sur le premier élément,
                // renvoyer le focus au dernier élément (boucle de navigation)
                if (event.shiftKey && document.activeElement === firstFocusableElement) {
                    lastFocusableElement.focus();
                    event.preventDefault();
                // Si "Tab" est pressé sans "Shift" et qu'on est sur le dernier élément,
                // renvoyer le focus au premier élément
                } else if (!event.shiftKey && document.activeElement === lastFocusableElement) {
                    firstFocusableElement.focus();
                    event.preventDefault();
                }
            }
        };
        // Ajoute un écouteur d'événements sur tout le document pour capturer les interactions clavier
        document.addEventListener("keydown", handleKeyPress);
        // Retourne une fonction pour nettoyer l'écouteur lorsque le composant est détruit
        // Par exemple lorsque sa condition {#if} devient false
        return () => document.removeEventListener("keydown", handleKeyPress);
    });
</script>

<header class="header">
    <a class="header-logo" href="/" use:link aria-label="Retour à l'accueil">
        <img class="logoWa" src={logoWa} loading="lazy" alt="Logo du site de Wendy Alverde">
    </a>

    <nav class="header-nav" aria-label="Navigation principale">
        <ul class="header-nav-list">
            <li><a href="/" use:link aria-label="Retour à l'accueil">Accueil</a></li>
            <li><a href="/portfolio" use:link aria-label="Aller sur la page portfolio">Portfolio</a></li>
            <li><a href="/contact" use:link aria-label="Aller sur la page contact">Contact</a></li>
            <li><a href="/cv" use:link aria-label="Aller sur la page CV">Mon CV</a></li>
        </ul>
    </nav>
    
    <section class="header-right">
        <ul class="socials" aria-label="Liens vers mes réseaux sociaux">
            <li>
                <a href="https://www.linkedin.com/in/wendy-alverde-850761237/" title="LinkdIn" target="_blank" aria-label="Lien vers LinkedIn">
                    <img class="socials__icon" src={linkedin} title="LinkdIn" alt="Lien vers mon profil LinkedIn">
                </a>
            </li>
            <li>
                <a href="https://github.com/WendyAlverde" target="_blank" aria-label="Lien vers GitHub">
                    <img class="socials__icon" src={github} title="GitHub" alt="Lien vers mon profil GitHub">
                </a>
            </li>
            <li>
                <a href="https://www.instagram.com/chat_push/" target="_blank" aria-label="Lien vers Instagram">
                    <img class="socials__icon" src={instagram} title="Instagram" alt="Lien vers mon profil Instagram">
                </a>
            </li>
        </ul>
    
        <button class="burger" aria-pressed={menuOpen} aria-label={menuOpen ? "Fermer le menu" : "Ouvrir le menu"} on:click={toggleMenu}>
            <em class="burger__bar"></em>
        </button>
        <!-- Mobile -->
        {#if menuOpen}
        <dialog class="accessibility" aria-modal="true" open>
            <button class="mobile" aria-label="Fermer le menu" on:click="{closeMenu}">
                <nav class="mobile-nav" >
                    <ul class="mobile-nav-list">
                        <li><a href="/" use:link aria-label="Aller sur la page d'accueil">Accueil</a></li>
                        <li><a href="/portfolio" use:link aria-label="Aller sur la page portfolio">Portfolio</a></li>
                        <li><a href="/contact" use:link aria-label="Aller sur la page contact">Contact</a></li>
                        <li><a href="/cv" use:link aria-label="Aller sur la page CV">Mon CV</a></li>
                    </ul>
                </nav>
            </button>
        </dialog>
        {/if}
        <!-- Mobile -->
    </section>
</header>

<style lang="scss">
    img[title]:hover::after {
        content: attr(title);
        position: absolute;
        top: -100%;
        left: 0;
        background-color: #0ace0a;
    }
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
        z-index: 2;

        @media (min-width: 770px) { /*PC*/
            padding: 0.8rem 2rem;
        }

        &-logo {

            .logoWa {
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
        }

        &-nav {
            display: none;
            
            @media (min-width: 710px) and (max-width: 991px) { /*Tablette et plus*/
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

                @media (min-width: 710px) { /*Passage du burger*/
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

            .accessibility {
                background: none;
                border: none;
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
    }
</style>