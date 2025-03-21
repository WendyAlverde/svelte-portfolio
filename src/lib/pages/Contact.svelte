<script>
    // les imports
    import { onMount } from "svelte";
    import emailjs from "emailjs-com";
    
    // Variables pour stocker les valeurs des inputs
    let firstname = "";
    let companyName = "";
    let email = "";
    let subject = "";
    let commentaire = "";
    let autorization = false;

    // Variables pour gérer les messages d'erreur
    let errorMessageEmail = "";
    let errorMessageCommentaire = "";

    // Fonction pour envoyer le formulaire
    function sanitizeInput(input) {
        return input.replace(/<script.*?>.*?<\/script>/gi, "") // Supprime tout script
                    .replace(/<\/?[^>]+(>|$)/g, ""); // Supprime toutes les balises HTML
    }

    // Fonction de validation de l'email
    function validateEmail() {
        console.log("Validation email:", email);
        if (email && !/^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$/.test(email)) {
            errorMessageEmail = "Veuillez entrer une adresse email valide.";
        } else {
            errorMessageEmail = "";  // Réinitialise le message d'erreur pour l'email
        }
    }

    // Fonction de validation du commentaire
    function validateCommentaire() {
        console.log("Validation commentaire:", commentaire);
        errorMessageCommentaire = commentaire.trim().length > 10
            ? ""
            : "Le message doit contenir au moins 10 caractères.";
    }

    // Fonction pour envoyer le formulaire
    function sendForm() {
        console.log("Formulaire envoyé");
        firstname = sanitizeInput(firstname);
        companyName = sanitizeInput(companyName);
        email = sanitizeInput(email);
        subject = sanitizeInput(subject);
        commentaire = sanitizeInput(commentaire);

        console.log("Données après nettoyage:", { firstname, companyName, email, subject, commentaire });

        if (!autorization) {
            alert("Vous devez consentir à la collecte de vos données.");
            return;
        }

        validateEmail();
        validateCommentaire();

        // Vérification des erreurs avant envoi
        console.log("Vérification des erreurs:", { errorMessageEmail, errorMessageCommentaire });

        if (!errorMessageEmail && !errorMessageCommentaire && autorization) {
            // Informations à envoyer
            let templateParams = {
                to_email: "wendy.alverde@outlook.com", // Remplacez par votre e-mail
                firstname,
                companyName,
                email,
                subject,
                commentaire
            };

            // Envoi via EmailJS
            console.log("Tentative d'envoi via EmailJS avec les paramètres :", templateParams);
            emailjs.send(
                "service_portfolio",
                "template_4t4x0fe",
                templateParams,
                "cwKfKOEJdoC7dFLV1"
            )
            .then(function(response) {
                console.log("Réponse EmailJS:", response);
                alert("Formulaire envoyé avec succès !");
            }, function(error) {
                console.log("Erreur EmailJS:", error);
                alert("Échec de l'envoi.");
            });
        } else {
            console.log("Erreur dans le formulaire !", { errorMessageEmail, errorMessageCommentaire, autorization });
        }
    }

    // Fonction pour ajuster la taille du textarea dynamiquement
    function adjustSize(event) {
        event.target.style.height = "auto";
        event.target.style.height = event.target.scrollHeight + "px";
    }
</script>

<main>
    <h1>Contact</h1>
    <p>Formulaire de contact pas encore fonctionnel, à venir</p>
    <section id="contact">
        <div class="section-header">
            <p>Je suis à la recherche d'une entreprise dynamique où je pourrai mettre mes compétences d'intégratrice web au service de projets innovants. Titulaire du titre professionnel de développeur web et web mobile depuis juin 2024.</p>
            <p>Utilisable prochainement</p>
        </div>
        <form class="form" on:submit|preventDefault={sendForm}>

            <!-- Nom et Prénom -->
            <label for="firstname">Nom, Prénom <span aria-hidden="true">*</span></label>
            <input type="text" name="firstname" id="firstname" placeholder="Nom, Prénom" bind:value={firstname} required>
        
            <!-- Nom de l'entreprise / Association -->
            <label for="companyName">Nom de l'entreprise ou association</label>
            <input type="text" name="companyName" id="companyName" placeholder="Nom de l'entreprise, association" bind:value={companyName}>
        
            <!-- Email -->
            <label for="email">Email <span aria-hidden="true">*</span></label>
            <input type="email" name="email" id="email" placeholder="Email" bind:value={email} on:blur={validateEmail} required>
            {#if errorMessageEmail}
                <p class="error-message" aria-live="polite">{errorMessageEmail}</p>
            {/if}
        
            <!-- Objet -->
            <label for="subject">Objet</label>
            <input type="text" name="subject" id="subject" placeholder="Objet" bind:value={subject}>
        
            <!-- commentaire -->
            <label for="commentaire">Message <span aria-hidden="true">*</span></label>
            <textarea name="commentaire" id="commentaire" placeholder="Message" bind:value={commentaire} on:input={adjustSize} required></textarea>
            {#if errorMessageCommentaire}
                <p class="error-message" aria-live="polite">{errorMessageCommentaire}</p>
            {/if}

            <div>
                <p class="obligatoire">Les champs marqués d'une astérisque (*) sont obligatoires.</p>
                <label class="autorization" for="autorization">
                    <input type="checkbox" name="autorization" id="autorization" bind:checked={autorization} required>
                    Je consens à la collecte de mes données personnelles conformément à la politique de confidentialité.
                </label>
            </div>
        
            <!-- Bouton d'envoi -->
            <button type="submit" class ={autorization ? "enabled" : "disabled"} disabled={!autorization}>Envoyer</button>
        </form>
    </section>
</main>

<style lang="scss">

</style>