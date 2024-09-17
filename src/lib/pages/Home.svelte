<script>
    // Import pictures
    // hero
    import profil from "../../assets/icons/site/home/profil/profil.webp"
    import hautbar from "../../assets/icons/site/home/paysages/hautbar.webp"
    import panier from "../../assets/icons/site/home/paysages/paniersoleil.webp"
    import montblanc from "../../assets/icons/site/home/paysages/montblanc.webp"
    // skills
    import figma from "../../assets/icons/site/home/imgskills/figma.webp"
    import github from "../../assets/icons/site/home/imgskills/github.webp"
    import css from "../../assets/icons/site/home/imgskills/css-3.webp"
    import html from "../../assets/icons/site/home/imgskills/html.webp"
    import javascript from "../../assets/icons/site/home/imgskills/js.webp"
    import svelte from "../../assets/icons/site/home/imgskills/svelte.webp"
    import react from "../../assets/icons/site/home/imgskills/react.webp"
    import vercel from "../../assets/icons/site/home/imgskills/logo-vercel.svg"
    import docker from "../../assets/icons/site/home/imgskills/docker.webp"
    import vsc from "../../assets/icons/site/home/imgskills/vsc.webp"
    import construct3 from "../../assets/icons/site/home/imgskills/construct3.svg"
    import piskel from "../../assets/icons/site/home/imgskills/piskel.webp"
    import photoshop from "../../assets/icons/site/home/imgskills/photoshop.webp"
</script>

<main>
    <!-- Profil -->
    <section id="hero">
        <div class="left">
            <h1>Intégratrice Web</h1>
            <p class="subtitle">Bonjour, je m'appelle Wendy Alverde</p>
            <p>Passionnée par la création et l'optimisation d'interface utilisateur, je suis à la recherche d'un poste en tant qu'Intégratrice Web aux alentours de Colmar. </p>
        </div>
        <div class="troisPhotos">
            <img src={hautbar} loading="lazy" alt="">
            <img src={panier} loading="lazy" alt="">
            <img src={montblanc} loading="lazy" alt="">
        </div>
        <p class="subtitlePicture" aria-hidden="true">Photographie prise par Wendy Alverde</p>
    </section>
    <!-- About -->
    <section id="about">
        <img class="profilpicture" src={profil} loading="lazy" alt="Profil de Wendy Alverde">
        <h2 class="section-title">À propos</h2>
        <h3>Qui suis-je</h3>
        <section class="text">
            <p>Après avoir étudié en foresterie au Québec pendant 4 ans, j'ai développé un vif intérêt pour les <em>aspects informatiques</em>, tels que la photo-interprétation et la géomatique.</p>
            <p> De retour en France il y a 3 ans, je suis fascinée par les coulisses des <em>effets spéciaux</em> cinématographiques et les <em>mystères de la création des pages web et des jeux vidéo</em>.</p>
            <p>Au cours de l'année 2022 et 2023, je me suis consacrée à une formation en autodidacte, en explorant diverses ressources telles que des <em>tutoriels sur YouTube</em> et des <em>cours en ligne sur OpenClassroom</em>. J'ai également suivi une formation intitulée "Initiation aux métiers du numérique" avec le CCI Campus de Strasbourg.</p>
            <p>Fin 2023 à avril 2024, j'ai suivi les cours chez O'clock, et  j'ai passé le <em>Titre Professionnel de Développeur Web et Web Mobile</em> de niveau Bac+2 en juin 2024.</p>
            <p>Ainsi, je souhaite travailler en tant qu'<em>Intégratrice web</em>.</p> <!--Mettre texte aligné (<br> pour passer à la ligne à la fin de celle-ci, si besoin)-->
        </section>
        <h3>Mes valeurs :</h3>
        <ul class="text">
            <li class="li1"><em>Créativité</em> : J'ai la capacité d'imaginer, concevoir et produire des idées originales et innovantes.</li>
            <li class="li2"><em>Plaisir</em> : J'apprécie chaque aspect de mon travail, ce qui se reflète dans ma motivation, ma satisfaction et ma capacité à donner le meilleur de moi-même.</li>
            <li class="li3"><em>Responsabilité écologique</em> : Je m'engage pour un travail respectueux de l'environnement en adoptant des pratiques durables et éco-responsables.</li>
            <li class="li4"><em>Rigueur</em> : J'aborde chaque projet avec une attention méticuleuse aux détails et à la qualité de mon travail.</li>
        </ul>              
    </section>
    <!-- Skills -->
    <section id="skills">
        <header>
            <h2 class="section-title">Mes compétences</h2>
            <p>Grâce à mes expériences professionnelles, j'ai développé des compétences telles que l'autonomie, la minutie et la préoccupation pour la sécurité.</p>
            <p>Voici un aperçu de mes compétences acquises par passion et par auto-formation.</p>
        </header>
        <div class="itemskills">
            <h3>Domaines de compétences</h3>
            <ul>
                <li>
                    <h4>Programmation</h4>
                    <p>Développement web et web mobile</p>
                </li>
                <li>
                    <h4>Photographie</h4>
                    <p>Photo de lieux historiques, paysage et macro nature</p>
                </li>
                <li>
                    <h4>Dessin</h4>
                    <p>Imagination débordante, œuvres uniques et originales</p>
                </li>
            </ul>
        </div>
        <div class="item">
            <h3>Outils de développement</h3>
            <div class="imgskills">
                <img src={html} loading="lazy" alt="Logo HTML">
                <img src={css} loading="lazy" alt="Logo CSS">
                <img src={javascript} loading="lazy" alt="Logo Javascript">
                <img src={github} loading="lazy" alt="Logo Github">
                <img src={vsc} loading="lazy" alt="Logo Visual Studia Code">
                <img src={react} loading="lazy" alt="Logo de la bibliothèque React">
                <img src={svelte} loading="lazy" alt="Logo du framework Svelte">
                <img src={vercel} loading="lazy" alt="Logo du site de déploiement Vercel">
                <img src={docker} loading="lazy" alt="Logo de Docker">
                <img src={construct3} loading="lazy" alt="Logo Construct3">
            </div>
            <h3>Outils de conception graphique</h3>
            <div class="imgskills">
                <img src={piskel} loading="lazy" alt="Logo Piskel">
                <img src={figma} loading="lazy" alt="Logo Figma">
                <img src={photoshop} loading="lazy" alt="Logo Photoshop">
            </div>
        </div>
    </section>
</main>

<style lang="scss">
    h1 {
        margin-top: 2rem;
    }

    h2 {
        padding-top: 1rem;
    }

    em {
        font-weight: bold;
    } 

    li {
        margin: 1rem;
    }

    // ====  Hero  ==== //
    #hero {
        background-color: var(--color-hero);
        display: flex;
        flex-direction: column;
        text-align: center;

        .subtitle {
            font-weight: bold;
            font-size: 1.5rem;
            margin: 2rem 0;
        }

        p {
            color: var(--text-clair);
        }

        // ====  Pictures  ==== //
        .troisPhotos {
            display: flex;
            justify-content: space-between;
            margin: 1rem 1rem 0;
        }

        img {
            width: 5.5rem;
            height: 3.5rem;
            object-fit: cover;
        }

        .subtitlePicture {
            font-size: 0.8rem;
            margin: 0.3rem 0 1rem;
        }
    }

    // ====  About  ==== //
    #about {
        padding: 1.5rem 0;
        display: flex;
        align-items: center;
        flex-direction: column;
        
        .profilpicture {
            width: 12rem;
        }

        h3 {
            margin-top: 1.2rem;
            padding-top: 0.5rem;
            border-top: 0.2rem solid var(--color-hero);
        }

        .text {
            padding: 1rem;
        }

        p  {
            word-spacing: 0.2rem;
        }
    }

    // ====  Skills  ==== //
    #skills {
        background-color: var(--text-clair);

        header p {
            font-weight: bold;
            text-align: center;
            margin-bottom: 1.2rem;
        }

        .itemskills {
            background-color: var(--text-clair);
            padding: 1rem 0;
        }

        // ====  logicels  ==== //
        .item {
            margin: 1rem;
            
            .imgskills {
                display: flex;
                flex-wrap: wrap;
                justify-content: center;
                
                img {
                    width: 4rem;
                    height: 4rem;
                    object-fit: cover;
                    margin: 1rem 0.5rem;
                }
            }
        }
    }

    // ========================= Responsive : Desktop ========================= //
    @media screen and (min-width: 769px) { /*PC*/
        .imgskills {

            img:hover {
                width: 5.5rem;
                height: 5.5rem;
            }
        }
    }
    
</style>