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
        firstname = sanitizeInput(firstname);
        companyName = sanitizeInput(companyName);
        email = sanitizeInput(email);
        subject = sanitizeInput(subject);
        commentaire = sanitizeInput(commentaire);

        if (!autorization) {
            alert("Vous devez consentir à la collecte de vos données.");
            return;
        }

        validateEmail();
        validateCommentaire();

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
            emailjs.send(
                "service_portfolio",
                "template_zf7vnhr",
                templateParams,
                "cwKfKOEJdoC7dFLV1"
            )
            .then(function(response) {
                alert("Formulaire envoyé avec succès !");
            }, function(error) {
                alert("Échec de l'envoi.");
            });
        } else {
            console.log("Erreur dans le formulaire !");
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
    <p>Vous avez un projet de site web ou d'application ? Que vous soyez un particulier, une association ou une entreprise, je suis là pour vous accompagner dans sa réalisation. N'hésitez pas à me contacter pour en discuter !</p>

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
            <p class="obligatoire">Les champs marqués d'une astérisque (<span aria-hidden="true">*</span>) sont obligatoires.</p>
            <label class="autorization" for="autorization">
                <input type="checkbox" name="autorization" id="autorization" bind:checked={autorization} required>
                Je consens à la collecte de mes données personnelles conformément à la politique de confidentialité.
            </label>
        </div>
    
        <!-- Bouton d'envoi -->
        <button type="submit" class ={autorization ? "enabled" : "disabled"} disabled={!autorization}>Envoyer</button>
    </form>
</main>

<style lang="scss">
    main {
        padding: 0 0.5rem;
        text-align: center;
        background-color: var(--bleugris-clair);

        p {
            color: var(--color-text);
        }

        form {
            background: var(--background-body);
            padding: 1.25rem;
            border-radius: 0.6rem;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
            text-align: left;

            label {
                font-weight: bold;
                color: var(--color-text);
                display: block;
                margin: 0.625rem 0 0.312rem;

                span {
                    color: var(--error);
                }
            }

            input, textarea {
                width: 100%;
                padding: 0.625rem;
                border: 0.0625rem solid #548072ab;
                border-radius: 0.3rem;
            }

            input:focus, textarea:focus {
                border-color: var(--blue-green);
                outline: none;
            }

            textarea {
                min-height: 8rem;
            }

            .error-message {
                color: var(--error);
                font-size: 0.9rem;
                margin: 0;
                padding: 0.2rem 0.1rem;
            }

            .obligatoire {
                font-size: 0.9rem;
                color: var(--color-text);
                margin: 0;
                padding: 0.2rem 0.1rem;

                span {
                    color: var(--error);
                }
            }

            .autorization {
                display: flex;
                align-items: center;
                font-size: 0.9rem;
                color: var(--color-text);
            }

            button {
                width: 100%;
                background: var(--blue-green);
                color: #fff;
                border: none;
                padding: 12px;
                font-size: 1rem;
                border-radius: 5px;
                cursor: pointer;
                margin-top: 15px;
                transition: background 0.3s ease-in-out;
            }

            button.disabled {
                background: #ccc;
                cursor: not-allowed;
            }

            button.enabled:hover {
                background: var(--blue-skills);
            }
        }
    }
</style>