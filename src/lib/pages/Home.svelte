<script>
    import {link} from "svelte-spa-router";
    import tools from "../../json/tools.json";
    // -------- Import pictures
    // hero
    import profil from "../../assets/site/home/profil/profil.webp";
    // -- mobile
    import hautbar from "../../assets/site/home/paysages/hautbar.webp";
    import panier from "../../assets/site/home/paysages/paniersoleil.webp";
    import montblanc from "../../assets/site/home/paysages/montblanc.webp";
    // -- desktop
    import nature1 from "../../assets/site/home/paysages/nature1.webp";
    import lacQuebec from "../../assets/site/home/paysages/lacQuebec.webp";
    import tourtelegraphe from "../../assets/site/home/paysages/tourtelegraphe.webp";
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
    <section class="about">
        <img class="about-profilpicture" src={profil} loading="lazy" alt="Photo de profil de Wendy Alverde, intégratrice web">
        <section class="about-articles">
            <h2>À propos</h2>
            <article>
                <h3>Qui suis-je</h3>
                <section class="about-articles-text">
                    <h4>Québec</h4>
                    <p class="about-articles-text-style">Après avoir étudié en foresterie au Québec pendant 4 ans, j'ai développé un vif intérêt pour les <em>aspects informatiques</em>, tels que la photo-interprétation et la géomatique.</p>
                    <!-- <h4>France</h4> -->
                    <h4>Passion</h4>
                    <p class="about-articles-text-style" >De retour en France il y a 4 ans, j'ai découvert une passion pour les <em>mystères de la création des pages web et des jeux vidéo</em>.</p>
                    <h4>Auto-formation</h4>
                    <p class="about-articles-text-style" >Au cours de l'année 2022 et 2023, je me suis formée en autodidacte en explorant diverses ressources telles que des <em>tutoriels sur YouTube</em> et des <em>moocs sur OpenClassroom</em>. J'ai également suivi une formation intitulée "Initiation aux métiers du numérique" avec le CCI Campus de Strasbourg.</p>
                    <h4>Formation O'clock</h4>
                    <p class="about-articles-text-style" >De octobre 2023 à avril 2024, j'ai suivi les cours chez O'clock, et  j'ai passé le <em>Titre Professionnel de Développeur Web et Web Mobile</em> de niveau Bac+2 en juin 2024.</p>
                    <h4>Formation Construct</h4>
                    <p class="about-articles-text-style" >En juillet, j'ai suivi une courte formation sur le <em>développement de jeux vidéo</em> avec l'application Construct. Cette expérience a été très enrichissante, m'apportant de nouvelles connaissances et m'aidant à développer une meilleure logique.</p>
                    <h4>Projet professionnel</h4>
                    <p class="about-articles-text-style" >Depuis, je travaille sur plusieurs projets de sites web pour continuer à pratiquer, approfondir mes compétences et rester à jour avec les dernières technologies. Je vous invite à découvrir mes projets sur la page <a href="/portfolio" use:link aria-label="Aller sur la page portfolio">Portfolio</a>.</p>
                    <h4>Auto-entrepreneur / Freelance</h4>
                    <p class="about-articles-text-style" >Ainsi, je souhaite travailler sur vos projets en tant qu'<em>Intégratrice web</em>.</p>
                </section>
            </article>
            <article>
                <h3>Mes valeurs :</h3>
                <ul class="about-articles-text" role="list">
                    <li class="about-articles-text-style" role="listitem"><em>Créativité</em> : J'ai la capacité d'imaginer, concevoir et produire des idées originales et innovantes.</li>
                    <li class="about-articles-text-style" role="listitem"><em>Plaisir</em> : J'apprécie chaque aspect de mon travail, ce qui se reflète dans ma motivation, ma satisfaction et ma capacité à donner le meilleur de moi-même.</li>
                    <li class="about-articles-text-style" role="listitem"><em>Responsabilité écologique</em> : Je m'engage pour un travail respectueux de l'environnement en adoptant des pratiques durables et éco-responsables.</li>
                    <li class="about-articles-text-style" role="listitem"><em>Rigueur</em> : J'aborde chaque projet avec une attention méticuleuse aux détails et à la qualité de mon travail.</li>
                </ul>         
            </article>
        </section> 
    </section>
    <!-- Skills -->
    <section class="skills">
        <header>
            <h2>Mes compétences</h2>
            <p>Grâce à mes expériences professionnelles, j'ai développé des compétences telles que l'autonomie, la minutie et la préoccupation pour la sécurité.</p>
            <p class="small">Voici un aperçu de mes compétences acquises par passion et par auto-formation.</p>
        </header>
        <section class="skills-items">
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
        </section>
        <section class="skills-tools">
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
        </section>
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
                display: flex;
                flex-direction: column;
                align-items: center;
                width: 70%; 
                padding-left: 1rem;
            }
            
            p {
                color: var(--text-black);
                max-width: 50rem;
            }  
        }

        &-right {
            width: 100vw;
            display: flex;
            flex-direction: column;
            align-items: center;

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

            .mobile {
                display: flex;

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
                        top: -5rem;
                        right: -4rem;
                        z-index: 1;
                    }
                    &-photo2 {
                        position: relative;
                        top: -1rem;
                        right: 2rem;
                    }
                    &-photo3 {
                        position: absolute;
                        bottom: -3rem;
                        right: -4rem;
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
                    top: 21.5rem;
                    right: 2.5rem;
                    font-size: 1rem;
                }
            }  
        } 
    }

    // ====  About  ==== //
    .about {
        background-color: var(--background-entete);
        padding: 1.5rem 0;
        display: flex;
        align-items: center;
        flex-direction: column;
        

        @media (min-width: 991px) { /*PC*/
            flex-direction: row;
            align-items: flex-start;
            position: relative;
            padding: 2rem;
        }
        
        &-profilpicture {
            width: 12rem;

            @media (min-width: 991px) { /*PC*/
                width: 24rem;
                flex-shrink: 0; /*Empêche l'image de rétrécir*/
                position: sticky;
                top: 6rem; /*Pour laisser de l'espace entre le header et la photo*/
            }
        }

        &-articles {
            h3 {
                margin-top: 1.2rem;
                padding-top: 0.5rem;
                border-top: 0.2rem solid var(--color-text);
                width: fit-content;
                // Pour centrer horizontalement l'élément
                margin-left: auto;
                margin-right: auto
            }

            &-text {
                padding: 1rem;

                @media (min-width: 991px) { /*PC*/
                    padding: 0.8rem 0 1rem 1.5rem;
                }

                // h4 {
                //     text-align: left;
                //     margin-left: 1rem;
                //     font-size: 0.9rem;
                //     margin-top: 0.2rem;
                //     font-style: italic;
                //     max-width: 20rem;
                //     padding-left: 0.5rem;
                //     border: 0.2rem solid var(--color-hero);
                //     border-image: linear-gradient(to right, var(--color-hero), transparent) 1;
                // }

                h4 {
                    position: relative;
                    padding: 0.5rem; /* Ajouter un espace intérieur */
                    border-radius: 5rem; /* Arrondir les coins */
                    background: linear-gradient(to right, var(--color-hero), #5480728c, #54807249, transparent);
                }

                h4::before {
                    content: " ";
                    position: absolute;
                    top: 0;
                    left: 0;
                    right: 0;
                    bottom: 0;
                    border-radius: 5rem;
                    background: white; /* Couleur de fond interne (ou autre couleur) */
                    z-index: -1;
                }

                &-style { 
                    text-align: justify;
                    hyphens: auto;
                    word-break: keep-all;
                    letter-spacing: 0.02rem;
                    word-spacing: 0.2rem;
                    font-size: 1rem;
                    margin: 0 1rem 0.8rem ;
                    padding-top: 0.3rem;

                    @media (min-width: 1300px) { /*PC*/
                        font-size: 1.2rem;
                    }
                    a {
                        color: var(--text-black);
                        font-weight: bold;
                    }
                }
            }
        }
    }

    // ====  Skills  ==== //
    .skills {
        padding-bottom: 0.02rem;
        margin: 0 0.5rem;

        header {
        
            p {
                font-weight: bold;
                text-align: center;
                letter-spacing: 0.02rem;
            }

            .small {
                font-size: 0.8rem;
            }

        }

        // ====  Compétences  ==== // 
        &-items {
            padding: 1rem 0;
        }

        // ====  Logiciels  ==== //
        &-tools {
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