<script>
    import {link} from "svelte-spa-router";
    import tools from "../../json/tools.json"
    // -------- Import pictures
    // hero
    import profil from "../../assets/site/home/profil/profil.webp"
    // -- mobile
    import hautbar from "../../assets/site/home/paysages/hautbar.webp"
    import panier from "../../assets/site/home/paysages/paniersoleil.webp"
    import montblanc from "../../assets/site/home/paysages/montblanc.webp"
    // -- desktop
    import nature1 from "../../assets/site/home/paysages/nature1.webp"
    import lacQuebec from "../../assets/site/home/paysages/lacQuebec.webp"
    import tourtelegraphe from "../../assets/site/home/paysages/tourtelegraphe.webp"
    // skills
    import figma from "../../assets/site/home/imgskills/figma.webp"
    import github from "../../assets/site/home/imgskills/github.webp"
    import css from "../../assets/site/home/imgskills/css-3.webp"
    import html from "../../assets/site/home/imgskills/html.webp"
    import javascript from "../../assets/site/home/imgskills/js.webp"
    import svelte from "../../assets/site/home/imgskills/svelte.webp"
    import react from "../../assets/site/home/imgskills/react.webp"
    import vercel from "../../assets/site/home/imgskills/logo-vercel.svg"
    import docker from "../../assets/site/home/imgskills/docker.webp"
    import vsc from "../../assets/site/home/imgskills/vsc.webp"
    import construct3 from "../../assets/site/home/imgskills/construct3.svg"
    import piskel from "../../assets/site/home/imgskills/piskel.webp"
    import photoshop from "../../assets/site/home/imgskills/photoshop.webp"
</script>

<main>
    <!-- Profil -->
    <section class="hero">
        <div class="hero-left">
            <h1>Intégratrice Web - Freelance</h1>
            <p>Wendy Alverde</p>
            <p>Passionnée par la création et l'optimisation d'interface utilisateur, je suis à la recherche de nouveaux projets de sites à créer ou à améliorer.</p>
            
        </div>
        <div class="hero-right">
            <div class="hero-right-troisPhotos mobile">
                <img class="hero-right-troisPhotos-myPhoto" src={hautbar} loading="lazy" title="Chateau du Haut-Bar" alt="" aria-hidden="true">
                <img class="hero-right-troisPhotos-myPhoto" src={panier} loading="lazy" title="Montgolfière lors du Mondial Air Ballons 2023 à Chambley" alt="" aria-hidden="true">
                <img class="hero-right-troisPhotos-myPhoto" src={montblanc} loading="lazy" title="Mont Blanc" alt="" aria-hidden="true">
            </div>
            <div class="hero-right-troisPhotos pc">
                <img class="hero-right-troisPhotos-myPhoto pc-photo1 " src={nature1} loading="lazy" alt="" aria-hidden="true">
                <img class="hero-right-troisPhotos-myPhoto pc-photo2 " src={lacQuebec} loading="lazy" title="Un lac au Québec" alt="" aria-hidden="true">
                <img class="hero-right-troisPhotos-myPhoto pc-photo3 " src={tourtelegraphe} loading="lazy" title="Tour télégraphe Chappe à saverne dans la Bas-Rhin" alt="" aria-hidden="true">
            </div>
            <p class="hero-right-subtitlePicture" aria-hidden="true">Photographie prise par Wendy Alverde</p>
        </div>
    </section>
    <!-- About -->
    <section id="about">
        <img class="profilpicture" src={profil} loading="lazy" alt="Photo de profil de Wendy Alverde, intégratrice web">
        <h2 class="section-title">À propos</h2>
        <article>
            <h3>Qui suis-je</h3>
            <section class="text">
                <p>Après avoir étudié en foresterie au Québec pendant 4 ans, j'ai développé un vif intérêt pour les <em>aspects informatiques</em>, tels que la photo-interprétation et la géomatique.</p>
                <p>De retour en France il y a 4 ans, j'ai découvert une passion pour les <em>mystères de la création des pages web et des jeux vidéo</em>.</p>
                <p>Au cours de l'année 2022 et 2023, je me suis formée en autodidacte en explorant diverses ressources telles que des <em>tutoriels sur YouTube</em> et des <em>moocs sur OpenClassroom</em>. J'ai également suivi une formation intitulée "Initiation aux métiers du numérique" avec le CCI Campus de Strasbourg.</p>
                <p>De octobre 2023 à avril 2024, j'ai suivi les cours chez O'clock, et  j'ai passé le <em>Titre Professionnel de Développeur Web et Web Mobile</em> de niveau Bac+2 en juin 2024.</p>
                <p>En juillet, j'ai suivi une courte formation sur le développement de jeux vidéo avec l'application Construct. Cette expérience a été très enrichissante, m'apportant de nouvelles connaissances et m'aidant à développer une meilleure logique.</p>
                <p>Depuis, je travaille sur plusieurs projets de sites web pour continuer à pratiquer, approfondir mes compétences et rester à jour avec les dernières technologies. Je vous invite à découvrir mes projets sur ma page <a href="/portfolio" use:link aria-label="Aller sur la page portfolio">Portfolio</a>.</p>
                <p>Ainsi, je souhaite travailler sur vos projets en tant qu'<em>Intégratrice web</em>.</p>
                <!--Mettre texte aligné (<br> pour passer à la ligne à la fin de celle-ci, si besoin) ou &nbsp; pour simuler un espace mais garder les éléments sur la même ligne-->
            </section>
        </article>
        <article>
            <h3>Mes valeurs :</h3>
            <ul class="text" role="list">
                <li class="li1" role="listitem"><em>Créativité</em> : J'ai la capacité d'imaginer, concevoir et produire des idées originales et innovantes.</li>
                <li class="li2" role="listitem"><em>Plaisir</em> : J'apprécie chaque aspect de mon travail, ce qui se reflète dans ma motivation, ma satisfaction et ma capacité à donner le meilleur de moi-même.</li>
                <li class="li3" role="listitem"><em>Responsabilité écologique</em> : Je m'engage pour un travail respectueux de l'environnement en adoptant des pratiques durables et éco-responsables.</li>
                <li class="li4" role="listitem"><em>Rigueur</em> : J'aborde chaque projet avec une attention méticuleuse aux détails et à la qualité de mon travail.</li>
            </ul>         
        </article>
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
            <ul role="list">
                <li role="listitem">
                    <h4>Programmation</h4>
                    <p>Développement de site web et web mobile</p>
                    <p>Développement de jeux vidéo</p>
                </li>
                <li role="listitem">
                    <h4>Photographie</h4>
                    <p>Photo de lieux historiques, paysage et macro nature</p>
                </li>
                <li role="listitem">
                    <h4>Dessin</h4>
                    <p>Imagination débordante, œuvres uniques et originales</p>
                </li>
            </ul>
        </div>
        <div class="item">
            <h3>Outils de développement</h3>
            <p>L'apprentissage continu est au cœur de mon parcours, car l'évolution des outils et des pratiques ne s'arrête jamais.</p>
            <div class="imgskills">
                {#each tools.devTools as devTool}
                    <div class="circularProgress">
                        <img class="iconsTools" src={devTool.src} loading="lazy" title={devTool.name} alt={devTool.alt}>
                    </div>
                {/each}
            </div>
            <h3>Outils de conception graphique</h3>
            <div class="imgskills">
                {#each tools.designTools as designTool}
                    <div class="circularProgress">
                        <img class="iconsTools" src={designTool.src} loading="lazy" title={designTool.name} alt={designTool.alt}>
                    </div>
                {/each}
            </div>
        </div>
    </section>
</main>

<style lang="scss">
    em {
        font-weight: bold;
    } 

    li {
        margin: 1rem;
    }

    // ====  Hero  ==== //
    .hero {
        background-color: var(--color-hero);
        display: flex;
        flex-direction: column;
        text-align: center;
        align-items: center;

        @media (min-width: 991px) { /*PC*/
            flex-direction: row; 
            height: 20rem;
        }

        &-left {
            @media (min-width: 991px) { /*PC*/
                width: 70%; 
            }
            
            p {
                color: var(--text-black);
            }  
        }

        &-right {
            width: 100vw;
            display: flex;
            flex-direction: column;
            align-items: center;
            padding-right: 4rem;

            @media (min-width: 991px) { /*PC*/
                width: 50%; 
            }

            // ====  Pictures  ==== //
            &-troisPhotos {
                display: flex;
                justify-content: space-between;
                margin: 1rem 1rem 0;
                width: 100%;
                max-width: 90%;

                @media (min-width: 991px) { /*PC*/
                    flex-direction: column;
                    align-items: center;
                }

                &-myPhoto {
                    width: 5.5rem;
                    height: 3.5rem;
                    object-fit: cover;

                    @media (min-width: 426px) { /*Tablette*/
                        width: 7rem;
                        height: 5rem;
                    }
                    @media (min-width: 710px) { /*Tablette*/
                        width: 9rem;
                        height: 7rem;
                    }
                }  
            }
            
            .pc {
                display: none;

                @media (min-width: 991px) { /*PC*/
                    display: flex;
                    position: relative;
                    width: auto;
                    height: auto;

                    .hero-right-troisPhotos-myPhoto {
                        width: 7rem;
                        height: 5rem;
                    }
                    
                    &-photo1 {
                        position: absolute;
                        top: -4rem;
                        right: -6rem;
                        z-index: 1;
                    }
                    &-photo2 {
                        position: relative;
                    }
                    &-photo3 {
                        position: absolute;
                        bottom: -4rem;
                        right: -6rem;
                    }
                }
            }

            .mobile {
                display: flex;

                @media (min-width: 991px) { /*PC*/
                    display: none;
                }
            }

            &-subtitlePicture {
                font-size: 0.8rem;
                margin: 0.3rem 0 1rem;
                
                @media (min-width: 991px) { /*PC*/
                    position: absolute;
                    bottom: 3.5rem;
                    right: 5rem;
                    font-size: 1rem;
                }
            }  
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
            border-top: 0.2rem solid var(--color-text);
            width: fit-content;
            // Pour centrer horizontalement l'élément
            margin-left: auto;
            margin-right: auto
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
        background-color: var(--background-clair);
        padding-bottom: 0.02rem;

        header p {
            font-weight: bold;
            text-align: center;
            margin-bottom: 1.2rem;
        }

        .itemskills {
            padding: 1rem 0;

            p {
                text-align: center;
            }
        }

        // ====  logicels  ==== //
        .item {
            margin: 1rem;

            h3 {
                margin: 1rem;
            }

            p {
                text-align: center;
            }
            
            .imgskills {
                display: flex;
                flex-wrap: wrap;
                justify-content: center;

                // ====  circularProgress  ==== // 
                .circularProgress {
                    width: 7rem;
                    height: 7rem;
                    border-radius: 50%;
                    border: 1rem solid transparent;
                    background-color: var(--background-clair);
                    margin: 0.5rem;
                    display: flex;
                    justify-content: center;
                    box-shadow: inset 0 0.1rem 0.8rem var(--blue-skills);
                }
                
                .iconsTools {
                    max-width: 4.5rem;
                    max-height: 3rem;
                    object-fit: cover;
                    margin: 1rem 0.5rem;
                }                
            }
        }
    }
</style>