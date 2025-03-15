<script>
  import Router from 'svelte-spa-router';
  import Routes from './routes.svelte';
  import Header from './components/Header.svelte';
</script>

<Header />

<main class="p-6">
  <Routes/>
</main>
