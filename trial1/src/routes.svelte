<script>
  import Home from './pages/Home.svelte'; 
  // import Products from './pages/Products.svelte'
  import About from './pages/About.svelte';
  import ProductsDetails from './pages/ProductsDetails.svelte';
  let route = window.location.pathname;
  
  function updateRoute() {
    route = window.location.pathname;
  }

  window.addEventListener('popstate', updateRoute);
</script>

<div>
  {#if route === '/'}
    <Home />
  {:else if route === '/products'}
    <Products />
  {:else if route.startsWith('/product/')}
    <ProductsDetails id={route.split('/').pop()} />
  {:else}
    <h1>404 - Page Not Found</h1>
  {/if}
</div>