<script>
    import { onMount } from 'svelte';
    // import { useParams } from 'svelte-navigator';
  
    // let params = useParams();
    let product = null;
  
    onMount(async () => {
      const res = await fetch('/products.json');
      const products = await res.json();
      // product = products.find(p => p.id === Number(params.id));
    });
  </script>
  
  {#if product}
    <div class="product-detail">
      <img src={product.image} alt={product.name} class="product-image" />
      <h1>{product.name}</h1>
      <p class="product-description">{product.description}</p>
      <p class="product-price">${product.price}</p>
      <button class="buy-btn">Buy Now</button>
    </div>
  {:else}
    <p>Loading...</p>
  {/if}
  
  <style>
    .product-detail {
      text-align: center;
    }
  
    .product-image {
      width: 100%;
      max-width: 400px;
      border-radius: 8px;
    }
  
    .product-description {
      font-size: 1.1rem;
      margin: 10px 0;
    }
  
    .product-price {
      font-weight: bold;
      color: green;
      font-size: 1.5rem;
    }
  
    .buy-btn {
      background: blue;
      color: white;
      padding: 10px 20px;
      border: none;
      cursor: pointer;
      border-radius: 5px;
    }
  </style>
  