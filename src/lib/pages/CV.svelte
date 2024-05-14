<script>
    import {link} from "svelte-spa-router"
    import at from "../../assets/icons/cv/at.svg"
    import calendar from "../../assets/icons/cv/calendar.svg"
    import car from "../../assets/icons/cv/car.svg"
    import house from "../../assets/icons/cv/house.svg"
    import card from "../../assets/icons/cv/id-card.svg"
    import phone from "../../assets/icons/cv/phone.svg"
    import linkedin from "../../assets/icons/site/linkedin.svg"
    import github from "../../assets/icons/site/github.svg"
    import instagram from "../../assets/icons/site/instagram.svg"   
</script>
    
    <main>
        <h1>Mon Curriculum Vitae</h1>
        <section id="containerPerso">
            <div class="left">
                <img src="" alt="Photo de profil de Wendy Alverde">
                <!-- Ajout d'une photo perso (en webp)--> 
            </div>
            <div class="right"> 
                <p> de Wendy Alverde</p><!-- h1 en haut, subtitle juste en dessous centré -->
                <h2>Intégratrice web</h2>
            </div>      
        </section>

        <section id="containerInfos">
            <div class="left"><!-- Description -->
                <p>À la recherche d'un poste d'Intégratrice Web aux alentours de Colmar dès <em>juin 2024</em>. À cette date j'aurais passé mon <em>Titre Professionnel niveau Bac+2 de Développeuse Web et Web Mobile</em>.</p>
            </div>
            <div class="right"><!-- Info perso -->
                <ul>
                    <li>
                        <!-- Voir pour mettre les images et icons en bdd -->
                        <img class="icon" src={at}>
                        alverdew@gmail.com
                    </li> 
                    <li>
                        <img class="icon" src={phone}>
                        0784588343
                    </li>
                    <li>
                        <img class="icon" src={calendar}>
                        25 ans
                    </li>
                    <li>
                        <img class="icon" src={house}>
                        Rohr
                    </li>
                    <li>
                        <img class="icon" src={card}>
                        Permis B
                    </li>
                    <li>
                        <img class="icon" src={car}>
                        Véhicule personnel
                    </li>
                </ul>
                <h3>Socials</h3>
                <ul>
                    <li>
                        <img class="icon" src={linkedin} >
                        <a href="https://www.linkedin.com/in/wendy-alverde" alt="Lien vers mon profil LinkedIn">@wendy-alverde</a>
                    </li>
                    <li>
                        <img class="icon" src={github} >
                        <a href="https://github.com/WendyAlverde" alt="Lien vers mon profil GitHub">WendyAlverde</a>
                    </li>
                    <li>
                        <img class="icon" src={instagram} >
                        <a href="https://www.instagram.com/chat_push/" alt="Lien vers mon profil Instagram">chat_push</a>
                    </li>
                </ul>
            </div>
        </section>

        <section id="containerInteret">
            <div class="left">
                <h3>Informatique</h3> <!-- Le plus à gauche -->
                <article>
                    <h4>Autoformation 2022 - 2023</h4>
                    <ul>
                        <li>Futur Engineer : Python et Blockly</li>
                        <li>OpenClassrooms : Mooc HTML5, CSS3 et JavaScript</li>
                        <li>YouTube : Tutos HTML, CSS et JavaScript</li>
                    </ul>
                </article>
                <article>
                    <h4>Réalisation d'un portfolio 2023 - 2024</h4>
                    <ul>
                        <li>Écrire du code en HTML, CSS et JavaScript, utilisation de Svelte</li>
                        <li><a href="/portfolio" alt="Lien vers le portfolio" use:link></a></li>
                    </ul>
                </article>
            </div>
            
            <div class="right">
                <h3>Atouts</h3> <!-- Le plus à droite -->
                <ul>
                    <li class="atouts">Rigoureuse</li>
                    <li class="atouts">Capacité d'adaptation</li>
                    <li class="atouts">Autonome</li>
                    <li class="atouts">Travail d'équipe</li>
                    <li class="atouts">Sens de l'organisation</li>
                    <li class="atouts">Minutieuse</li>
                </ul>
            </div>
        </section>

        <section id="containerExperience">
            <div class="left">
                <h3>Diplômes et Formations</h3>
                <article>
                    <p><em>Développeur Web et Web Mobile</em> ― <span>O'Clock</span> | Distantiel</p>
                    <!-- Faire des articles pour chaque formation -->
                    <p class="date">Depuis octobre 2023</p>
                    <ul>
                        <li>HTML, CSS, Accessibilité, SEO</li>
                        <li>PHP</li>
                        <li>JavaScript - Svelte</li>
                        <li>Adminer -Directus</li>
                        <li>Docker</li>
                        <li>Commande terminal Linux</li>
                    </ul>
                </article>
                <article>
                    <p><em>Num & Boost</em> ― <span>CCI Campus</span> | Distantiel</p> 
                    <p class="date">De mars 2023 à avril 2023</p>
                    <ul>
                    <li>HTML, CSS, JavaScript</li>
                        <li>Algorithme</li>
                        <li>Cybersécurité</li>
                        <li>Marketing</li>
                    </ul>
                </article>
                <article>
                    <p><em>Études collégiales en technologie forestière</em> ― <span>Cégep</span> | Baie-Comeau,Canada</p>
                    <p class="date">D'août 2018 à février 2021</p>
                    <ul>
                        <li>Utilisation des logiciels : ArcGIS, QGIS, Excel, Word, LiDAR</li>
                    </ul>
                </article>
                <article>
                    <p><em>Études collégiales en technique d'aménagement cynégétique et halieutique</em> ― <span>Cégep</span> | Baie-Comeau, Canada</p>
                    <p class="date">D'août 2017 à juin 2018</p>
                </article>
                <article>
                    <p><em>Baccalauréat en science technique de l'industrie et développement durable</em> ― <span>Lycée Dhuoda</span> | Nîmes</p>
                    <p class="date">De septembre 2014 à juin 2016</p>
                    <ul>
                        <li>Option système informatique et numérique</li>
                    </ul>
                </article>
            </div>
            <div class="right">
                <h3>Expériences professionnelles</h3>
                <article>
                    <p><em>Agent d'entretien</em> ― <span>Alsa Bio Concept SAS</span> | Colmar</p>
                    <p class="date">De mai 2021 à septembre 2022</p>
                    <ul>
                        <li>Règles de sécurité et d'hygiène</li>
                        <li>Nettoyage intérieur et extérieur</li>
                        <li>Désinfection COVID</li>
                    </ul>
                </article>
                <article>
                    <p><em>Laborantine et ouvrière agricole</em> ― <span>Centre d’Expérimentation et de Développement en Forêt Boréal</span> | Baie-Comeau, Québec</p>
                    <p class="date">De mai 2020 à février 2021</p>
                    <ul>
                        <li>Préparation des champs et apiculture ponctuelle</li>
                        <li>Écriture d'un journal de bord</li>
                        <li>Décontamination, repiquage et multiplication de plantes</li>
                        <li>Fabrication de milieu et tourbe</li>
                    </ul>
                </article>
                <article>
                    <p><em>Laborantine</em> ― <span>Société de Protection des Forêts contre les Insectes et Maladies</span> | Baie-Comeau, Québec</p>
                    <p class="date">De juillet 2018 à août 2018</p>
                    <ul>
                        <li>Études des rapports entre insectes et branches en laboratoire</li>
                    </ul>
                </article>
            </div>
        </section>

        <section id="langues">
            <div class="left">
                <h3>Centres d'intérêt</h3> <!-- Au milieu -->
                <h4>Pratiques artistiques</h4>
                <ul>
                    <li>Photographie</li>
                    <li>Puzzle</li>
                    <li>Dessin</li>
                </ul>
                <h4>Voyages</h4>
                <ul>
                    <li>3 ans au Québec</li>
                    <li>Camping nature</li>
                    <li>Road trip</li>
                </ul>
                <h4>Activités sportives</h4>
                <ul>
                    <li>Ski</li>
                    <li>Randonnée</li>
                </ul>
            </div>
            <div class="right">
                <h3>Langues</h3>
                <h4>Anglais</h4>
                <p>Niveau A2</p>
            </div>
        </section> 
    </main> 

<style>
    * {
        box-sizing: border-box;
    }

    main {
        background-color: #eef7f4;
        text-align: center;
    }

    /* Permet de faire un condensé plutôt que répété les même choses dans chaques tagname, id, class */
    #containerPerso, #containerInfos, #containerInteret, #containerExperience, #langues {
        background-color: #d6e7e1;
        box-shadow: 0.3rem 0.3rem 0.3rem #9ab4ab;
        border-radius: 0.3rem;
        margin-bottom: 1rem;
    }

    /* Les titres, span, em */
    h1, h2, h3 {
        font-weight: bold;
        padding: 0.6rem;
        margin: 0.6rem;
        color: var(--blue-green);
    }

    h2, h3 {
        color: #019233;  
    }

    h4, em {
        font-weight: bold;
    }

    span {
        color: #019233;
    }

    img {
        width: 1rem;
    }



    @media screen and (min-width: 426px) and (max-width: 768px) { /*Tablette*/
        
    }

    @media screen and (min-width: 769px) { /*PC*/

    }

</style>
