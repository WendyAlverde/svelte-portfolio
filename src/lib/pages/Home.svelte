<script>
    import {link} from "svelte-spa-router"
    import profil from "../../assets/images/profil.webp"
    import mousse from "../../assets/images/mousse.webp"
    import tourtelegraphe from "../../assets/images/tourtelegraphe.webp"
    import pissenlit from "../../assets/images/pissenlit.webp"
</script>

<main>
    <section id="hero">
        <div class="containerHero">
            <div class="hero__item left">
                <h1>Intégratrice Web</h1>
                <p class="subtitle">Bonjour, je m'appelle Wendy Alverde</p>
                <p>Passionnée par la création et l'optimisation d'interface utilisateur, je suis à la recherche d'un poste en tant qu'Intégratrice Web aux alentours de Colmar. </p>
            </div>
            <div class="hero__item right">
                <div class="troisphotos">
                    <div class="photo photo1">
                        <img src={mousse} loading="lazy" alt="">
                    </div>
                    <div class="photo photo2">
                        <img src={tourtelegraphe} loading="lazy" alt="">
                    </div>
                    <div class="photo photo3">
                        <img src={pissenlit} loading="lazy" alt="">
                    </div>
                </div>
            </div>
        </div>
    </section>
    <section id="about">
        <div class="grid__item left">
            <img src={profil} loading="lazy" alt="Profil de Wendy Alverde">
        </div>
        <div class="grid__item right">
            <h2 class="section-title">À propos</h2>
            <h3>Qui suis-je</h3>
            
            <p>Après avoir étudié en foresterie au Québec pendant 4 ans, j'ai développé un vif intérêt pour les <em>aspects informatiques</em>, tels que la photo-interprétation et la géomatique. De retour en France il y a 3 ans, je suis fascinée par les coulisses des <em>effets spéciaux</em> cinématographiques, les <em>mystères de la création des pages web et des jeux vidéo</em>. Au cours de l'année 2022, je me suis consacrée à une formation en autodidacte, en explorant diverses ressources telles que des <em>tutoriels sur YouTube</em> et des <em>cours en ligne sur OpenClassroom</em>. J'ai également suivi une formation intitulée 'Initiation aux métiers du numérique' avec le CCI Campus. En 2023, j'ai suivi de cours chez O'clock, pour passer le <em>Titre Professionnel de Développeur Web et Web Mobile</em> de niveau Bac+2 en juin 2024. Ainsi, je souhaite travailler en tant qu'<em>Intégratrice web</em>.</p> <!--Mettre texte aligné (<br> pour passer à la ligne à la fin de celle-ci, si besoin)-->
            <h3>Mes valeurs :</h3>
            <ul>
                <li class="li1">Créativité : J'ai la capacité d'imaginer, concevoir et produire des idées originales et innovantes.</li>
                <li class="li2">Plaisir : J'apprécie chaque aspect de mon travail, ce qui se reflète dans ma motivation, ma satisfaction et ma capacité à donner le meilleur de moi-même.</li>
                <li class="li3">Responsabilité écologique : Je m'engage pour un travail respectueux de l'environnement en adoptant des pratiques durables et éco-responsables.</li>
                <li class="li4">Rigueur : J'aborde chaque projet avec une attention méticuleuse aux détails et à la qualité de mon travail.</li>
            </ul>              
        </div>
    </section>
    <section id="skills">
        <div class="section-hearder">
            <h2 class="section-title">Mes compétences</h2>
            <p class="pskills">Grâce à mes expériences professionnelles, j'ai développé des compétences telles que l'autonomie, la minutie et la préoccupation pour la sécurité. Voici un aperçu de mes compétences acquises par passion et par auto-formation.</p>
        </div>
        <div class="item">
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
            <h3>Compétences en développement</h3>
            <!-- Changer cette partie -->
            <div class="progressbar">
                <div class="bar" data-width="95">HTML</div>
            </div>
            <div class="progressbar">
                <div class="bar" data-width="85">CSS</div>
            </div>
            <div class="progressbar">
                <div class="bar" data-width="50">JAVASCRIPT</div>
            </div>
            <div class="progressbar">
                <div class="bar" data-width="30">PHP</div>
            </div>
            <h3>Compétences en conception graphique</h3>
            <div class="progressbar">
                <div class="bar" data-width="90">Piskel</div>
            </div>
            <div class="progressbar">
                <div class="bar" data-width="20">Photoshop</div>
            </div>
        </div>
    </section>
    <section id="portfolio">
        <h2>Portfolio</h2>
        <p>La programmation est la clé qui ouvre les portes du renouveau technologique, où l'imagination devient réalité et où les possibilités deviennent infinies.</p>
        <!--Essai/impro : 3 photos collées avec petite marge entre elles. Sur la photo, le titre et un lien 'voir plus'. Lorsqu'on clique sur 'voir plus' renvoi à une autre page-->
        <article>
            <img src="" alt="">
            <h3>O'Cook</h3>
            <a href="/ocook" use:link></a>
        </article>
    </section>
</main>

<style lang="scss">
    img {
        width: 8rem;
        height: 10rem;
        object-fit: cover;
    }

    .containerHero {
        background-color: var(--color-hero);
    }

    .containerHero p{
        color: var(--text-clair);
    }

    .subtitle {
        font-weight: bold;
        font-size: 1.5rem;
    }
</style>