<script>
  import Router from "svelte-spa-router"
  import Contact from "./lib/pages/Contact.svelte"
  import Home from "./lib/pages/Home.svelte"
  import NotFound from "./lib/pages/NotFound.svelte"
  import Portfolio from "./lib/pages/Portfolio.svelte"
  import Header from "./lib/components/Header.svelte"
  import Footer from "./lib/components/Footer.svelte"
  import LegalNotices from "./lib/pages/LegalNotices.svelte";
  import CV from "./lib/pages/CV.svelte";
  
const routes = {
  "/": Home,
  "/contact": Contact,
  "/portfolio": Portfolio,
  "/legal-notices": LegalNotices,
  "/cv": CV,
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