<script>
    import { onMount } from 'svelte';
    // import ProductCard from '../ents/ProductCard.svelte';
    import ProductCard from './../components/ProductCard.svelte'
  
    let products = [];
  
    onMount(async () => {
      const res = await fetch('/products.json'); // Adjust path if necessary
      products = await res.json();
    });
    console.log(products)
  </script>
  
  <h1>Our Products</h1>
  
  <div class="product-grid">
    {#each products as product}
      <ProductCard {product} />
    {/each}
  </div>
  
  <style>
    .product-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      gap: 20px;
    }
  </style>
  