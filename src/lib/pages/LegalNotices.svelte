<h2>Mentions Légales</h2>

<main role="main">
    <section class="identification" role="region" aria-labelledby="site-identification-heading">
        <div class="column first">
            <h3 id="site-identification-heading">Identification du site</h3>
            <p class="websiteid">Nom du site : Wendy Alverde - Portfolio</p>
            <p>Contact : <a href="mailto:alverdew@gmail.com" aria-label="Lien cliquable qui mène à votre boîte mail">alverdew@gmail.com</a></p>
            <p>Adresse : Rohr</p>
        </div>
        
        <div class="column">
            <h3 id="site-owner-heading" aria-describedby="site-owner-description">Propriétaire du site</h3>
            <p id="site-owner-description">Propriétaire : Wendy Alverde</p>

            <h3 id="copyright-heading" aria-describedby="droits d'auteurs et image">Droits d'auteur et images</h3>
            <p id="droit d'auteur et image">Les textes et photographies sont rédigés et prises par Wendy Alverde.</p>

            <h3>Conception et développement</h3>
            <p id="conception-developpement">Ce site a été conçu et développé par Wendy Alverde.</p> 
        </div>
    </section>

    <section role="region" aria-labelledby="Important-information">
        <div class="column first">
            <h3 id="personal-data-collection-heading" aria-describedby="collecte des données personnelles">Collecte de données personnelles</h3>
            <p id="collecte des données personnelles">Nous ne collectons aucune informations.</p>

            <h3 id="minor-protection-heading" aria-describedby="description de la protection des mineurs">Protection des mineurs</h3>
            <p id="description de la protection des mineurs">Ce site est pour toutes personnes intéressé par mon profil.</p>

            <h3 id="titre-hebergement">Hébergement du site</h3>
            <p id="hebergement-site">Ce site est hébergé sur la plateforme Vercel.</p>
        </div>

        <div class="column">
            <h3 id="cookies-heading" aria-describedby="description des cookies">Cookies</h3>
            <p id="description des cookies">Ce site n'utilise aucun cookie.</p>

            <h3 id="warning-heading" aria-describedby="description d'avertissement">Mise en garde</h3>
            <p id="description d'avertissement">Les informations fournies sur ce site sont données à titre indicatif et ne doivent pas se substituer à un avis professionnel.</p>
        </div>
    </section>
</main>

<style>
    p {
        line-height: 1.2rem;
        font-size: 1rem;
    }

    .identification {
        background-color: var(--text-clair);
    }
    .websiteid{
        font-weight: bold;
    }

    section {
        padding: 1rem; 
        text-align: justify-all;
        border-radius: 0.2rem;
        box-shadow: 0 0 5px #548072;
        text-align: center;
    }

    

    

    @media screen and (min-width: 426px) and (max-width: 768px) { /*Tablette*/
        section {
            display: flex;
        }
        .column {
            width: 50%;
        }
        .column.first {
            border-right: groove #548072 1px;
        }
    }

    @media screen and (min-width: 769px) { /*PC*/

    }

</style>

