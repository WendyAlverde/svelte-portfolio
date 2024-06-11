<script>
    import {link} from "svelte-spa-router"
    // import pictures
    import linkedin from "../../assets/icons/site/socials/linkedin.svg"
    import github from "../../assets/icons/site/socials/github.svg"
    import instagram from "../../assets/icons/site/socials/instagram.svg"
</script>

<header role="banner">
    <div class="container"> <!-- A retirer quand construction part -->
        <a class="logo" href="/" use:link>Wendy Alverde</a>
        <nav role="navigation">
            <ul class="menu list-unstyled">
                <li><a href="/" title="Cliquer pour aller sur la page d'accueil" use:link>Accueil</a></li>
                <li><a href="/portfolio" title="Cliquer pour aller sur la page portfolio" use:link>Portfolio</a></li>
                <li><a href="/contact" title="Cliquer pour aller sur la page contact" use:link>Contact</a></li>
                <li><a href="/cv" title="Cliquer pour aller sur la page de mon curriculum vitae" use:link>Mon CV</a></li>
            </ul>
        </nav>
        <ul class="socials">
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
        <button aria-pressed="false" class="burger"><em class="bar"></em></button>
    </div>
    <div class="banniere">
        <p>SITE EN CONSTRUCTION</p>
    </div>
</header>

<style lang="scss">
    header { 
        background: var(--background-entete);
        border-bottom: 1px solid #eee;
        border-radius: 0.3rem;
        box-shadow: 0 0 5px #548072; 
        position: sticky;
        top: 0;
        z-index: 1;
        margin-bottom: 1rem;
    }

    header .logo {
        font-family: 'Playfair Display', serif;
        letter-spacing: 1px;
    }

    .container {
        display: flex;
        justify-content: space-between;
        padding: 1rem 0.5rem;
        align-items: center;
    }

    a, ul {
        margin-top: 0.6rem;
    }

    nav {
        // display: flex;
        // justify-content: center;
        // align-items: center;
        // flex-direction: column;
        display: none;
        // position: fixed;
        // top: 3.4rem;
        // left: 110%;
        overflow: hidden;
        // height: calc(100vh -3.4rem);
        background: var(--background-entete);
        transition: all 0.4s ease-out;
    }


    header a  {
        color: var(--color-text);
        font-weight: bold;
    }

    header a:hover {
        color: var(--color-passagesouris);
    }

    .socials {
        display: flex;
    }

    /* Burger */
    .burger {
        background: none;
        border: none;
        width: 2.1rem;
        height: 2.1rem;
        cursor: pointer;
    }

    .burger .bar, .burger .bar::before, .burger .bar::after {
        display: block;
        content: "";
        width: 1.3rem;
        height: 0.2rem;
        background-color: var(--color-text);
        position: absolute;
    }

    .burger .bar::before {
        transform: translateY(-0.5rem);
    }

    .burger .bar::after {
        transform: translateY(0.5rem);
    }
    /* Ne restera pas à la fin */
    .banniere {
        background: #EBB300;
        border: 0.2rem solid #D47E00;
        border-radius: 0.3rem;
        box-shadow: 0 0 0.3rem #D47E00; /*Ombre*/
        position: sticky;
        top: 0;
        z-index: 1;
    }

    .banniere p {
        text-align: center;
    }
    /* Ne restera pas à la fin */

    @media screen and (min-width: 426px) and (max-width: 768px) { /*Tablette*/
        header .logo {
            font-size: 1.5rem;
            letter-spacing: 1px;
        }

        header li {
            font-size: 1.5rem;
            padding: 0 .5rem;
        }

        nav {
            display: block;
        }

        .burger {
            display: none;
        }
    }

    @media screen and (min-width: 769px) { /*PC*/
        header .logo {
            font-size: 2rem;
            letter-spacing: 2px;
        }
        header li {
            font-size: 2rem;
            padding: 0.5rem;
        }

        nav {
            display: block;
        }

        .burger {
            display: none;
        }

        nav .menu {
            display: flex;/*1*/
            flex-direction: row;/*2*/
            justify-content: space-around;/*3*/
            padding-top: 1rem;
        }
    }
</style>