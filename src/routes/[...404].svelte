<script context="module">
    export const load = ({ route }) => ({
        status: 404,
        error: '404 Stránka nenájdená',
        props: { url: route.url },
    })

    const isDev = import.meta.env?.DEV
</script>

<script>
    export let url
</script>

<!-- routify:meta inline=false -->

<!-- This file was created by Routify.
     To customize the error page, create a catchall page 
     in the root of your project. Eg. [...404].svelte -->
     <section>
    <h2>404 - Stránka nenájdená</h2>
    <p>
        Stránka <code>https://slovcontact.sk{url}</code> nebola nájdená. Skontrolujte webovú adresu alebo sa vráťte <a href="/">na domovskú stránku</a>.
    </p>
</section>

<style>
    section {
      margin-bottom: 2rem;
      background-color: #fff;
      padding-left: 2px;
    }
  
    h2 {
      color: #1a3c6e;
      border-bottom: 2px solid #1a3c6e;
      padding-bottom: 0.5rem;
    }
  </style>
  
