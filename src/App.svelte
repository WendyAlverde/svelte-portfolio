<script>
  // Importer le router
  import Router from "svelte-spa-router";

  // Importer les composants
  import Header from "./lib/components/Header.svelte";
  import Footer from "./lib/components/Footer.svelte";
  
  // Importer nos pages
  import Home from "./lib/pages/Home.svelte";
  import Portfolio from "./lib/pages/Portfolio.svelte";
  import Contact from "./lib/pages/Contact.svelte";
  import CV from "./lib/pages/CV.svelte";
  import LegalNotices from "./lib/pages/LegalNotices.svelte";
  import NotFound from "./lib/pages/NotFound.svelte";
  
const routes = {
  "/": Home,
  "/portfolio": Portfolio,
  "/contact": Contact,
  "/cv": CV,
  "/legal-notices": LegalNotices,
  "*": NotFound,
}

</script>

<div class="container"> 
  <Header />
  <Router {routes} />
  <Footer />
</div>



<style>
  /* Ne concerne que app Svelte */
</style>