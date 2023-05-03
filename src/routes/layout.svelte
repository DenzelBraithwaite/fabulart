<!-- src/routes/__layout.svelte -->
<svelte:head>
  <title>Fabulart Layout</title>
  <link rel="stylesheet" href="/global.css" hydrate />
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Ubuntu:ital,wght@0,300;0,400;0,700;1,300;1,400&display=swap" rel="stylesheet">
</svelte:head>

<main>    
  <slot />
</main>

<style>
  /* add global styles here */
  :global(body) {
    box-sizing: border-box;
    font-family: 'Ubuntu', sans-serif;
    padding: 0;
    margin: 0;
    color: #2e2e2e;
    /* line-height: 1; */
  }

  :global(h1,h2,p) {
    margin: 0;
  }

  /* font wasn't applying to form textarea fields */
  :global(textarea) {
    font-family: 'Ubuntu';
  }
</style>
