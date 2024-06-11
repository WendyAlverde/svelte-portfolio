<script>
    // Import pictures
    import profil from "../../assets/icons/site/profil/profil.webp"
    import pissenlit from "../../assets/icons/site/paysages/pissenlit.webp"
    import panier from "../../assets/icons/site/paysages/paniersoleil.webp"
    import montblanc from "../../assets/icons/site/paysages/montblanc.webp"
    import engrenage from "../../assets/icons/site/home/engrenage.webp"
</script>

<main role="main">
    <!-- Profil -->
    <section id="hero">
        <div class="left">
            <h1>Intégratrice Web</h1>
            <p class="subtitle">Bonjour, je m'appelle Wendy Alverde</p>
            <p>Passionnée par la création et l'optimisation d'interface utilisateur, je suis à la recherche d'un poste en tant qu'Intégratrice Web aux alentours de Colmar. </p>
        </div>
        <div class="troisPhotos">
            <div class="photo photo1">
                <img src={pissenlit} loading="lazy" alt="">
            </div>
            <div class="photo photo2">
                <img src={panier} loading="lazy" alt="">
            </div>
            <div class="photo photo3">
                <img src={montblanc} loading="lazy" alt="">
            </div>
        </div>
        <p class="subtitlePicture" aria-hidden="true">Photographie prise par Wendy Alverde</p>
    </section>
    <!-- About -->
    <section id="about">
        <img class="profilpicture" src={profil} loading="lazy" alt="Profil de Wendy Alverde">
        <h2 class="section-title">À propos</h2>
        <h3>Qui suis-je</h3>
        <p>Après avoir étudié en foresterie au Québec pendant 4 ans, j'ai développé un vif intérêt pour les <em>aspects informatiques</em>, tels que la photo-interprétation et la géomatique.</p>
        <p> De retour en France il y a 3 ans, je suis fascinée par les coulisses des <em>effets spéciaux</em> cinématographiques et les <em>mystères de la création des pages web et des jeux vidéo</em>.</p>
        <p>Au cours de l'année 2022 et 2023, je me suis consacrée à une formation en autodidacte, en explorant diverses ressources telles que des <em>tutoriels sur YouTube</em> et des <em>cours en ligne sur OpenClassroom</em>. J'ai également suivi une formation intitulée 'Initiation aux métiers du numérique' avec le CCI Campus de Strasbourg.</p>
        <p>Fin 2023 à avril 2024, j'ai suivi les cours chez O'clock, pour passer le <em>Titre Professionnel de Développeur Web et Web Mobile</em> de niveau Bac+2 en juin 2024.</p>
        <p>Ainsi, je souhaite travailler en tant qu'<em>Intégratrice web</em>.</p> <!--Mettre texte aligné (<br> pour passer à la ligne à la fin de celle-ci, si besoin)-->
        <h3>Mes valeurs :</h3>
        <ul>
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
            <p class="pskills">Grâce à mes expériences professionnelles, j'ai développé des compétences telles que l'autonomie, la minutie et la préoccupation pour la sécurité. Voici un aperçu de mes compétences acquises par passion et par auto-formation.</p>
        </header>
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
                <div class="bar" data-width="50">Figma</div>
            </div>
            <div class="progressbar">
                <div class="bar" data-width="20">Photoshop</div>
            </div>
        </div>
    </section>
</main>

<style lang="scss">
    // ====  Hero  ==== //
    #hero {
        background-color: var(--color-hero);
        display: flex;
        flex-direction: column;
        text-align: center;
    }
    h1 {
        margin-top: 2rem;
    }
    .subtitle {
        font-weight: bold;
        font-size: 1.5rem;
        margin: 2rem 0;
    }
    #hero p{
        color: var(--text-clair);
    }
    // ====  Pictures  ==== //
    .troisPhotos {
        display: flex;
        justify-content: space-between;
        margin: 1rem 1rem 0;
    }
    .photo img {
        width: 5.5rem;
        height: 3.5rem;
        object-fit: cover;
    }
    .subtitlePicture {
        font-size: 0.8rem;
        margin: 0.3rem 0 1rem;
    }
    // ====  About  ==== //
    #about {
        padding: 1.5rem 0;
        display: flex;
        align-items: center;
        flex-direction: column;
        background-color: var(--text-clair);
    }
    .profilpicture {
        width: 12rem;
    }
    
    h2 {
        margin-top: 1rem;
    }

    h3 {
        margin-top: 0.8rem;
    }
    #about p  {
        word-spacing: 0.2rem;
    }

    em {
        font-weight: bold;
    }    
    li {
        margin: 1rem;
    }
    // ====  About  ==== //
    header p {
        font-weight: bold;
    }
</style>