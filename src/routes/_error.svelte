<script>
  import Main from "../components/Main.svelte";
  import Footer from "../components/Footer.svelte";

  export let status;
  export let error;
  export let message;

  const dev = process.env.NODE_ENV === "development";
</script>

<style>
  .Error {
    padding: 4em 0 0 0;
  }

  h1,
  p {
    margin: 0 auto;
  }

  h1 {
    font-size: 2.8em;
    font-weight: 700;
    margin: 0 0 0.5em 0;
  }
</style>

<svelte:head>
  <title>No encontrada</title>
</svelte:head>

<Main>
  <div class="Error">
    <h1>
      {status}
    </h1>
    <p>{ status == 404 ? (message = 'Parece que no existe lo que buscas') : (message = 'Parece que hay un error con el servidor')}</p>
    {#if dev && error.stack}
      <pre>{error.stack}</pre>
    {/if}
  </div>
  <Footer />
</Main>
