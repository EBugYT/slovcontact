<script context="module">
  import { Router, createRouter } from "@roxi/routify";
  import Header from "./components/Header.svelte";
  import Footer from "./components/Footer.svelte";
  import routes from "../.routify/routes.default.js";

  export const router = createRouter({ routes });
</script>

<main>
  <Header />
  <Router {router} />
  <Footer />
</main>

<style>
  main {
    font-family: Arial, sans-serif;
    max-width: 1200px;
    margin: 0 auto;
    padding: 0;
    background-color: #ffffff;
  }
</style>
