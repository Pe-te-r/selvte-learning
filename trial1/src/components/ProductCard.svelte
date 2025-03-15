<script>
    // import { goto } from 'svelte-navigator';
    export let product;
  
    // function viewDetails() {
    //   goto(`/product/${product.id}`);
    // }
  </script>
  
  <div class="product-card">
    <img src={product.image} alt={product.name} class="product-image" />
    <h2 class="product-name">{product.name}</h2>
    <p class="product-description">{product.description}</p>
    <p class="product-price">${product.price}</p>
    
    <button class="buy-btn">Buy Now</button>
    <!-- <button class="more-btn" on:click={viewDetails}>More</button> -->
  </div>
  
  <style>
    .product-card {
      border: 1px solid #ddd;
      border-radius: 8px;
      padding: 16px;
      text-align: center;
    }
  
    .product-image {
      width: 100%;
      max-height: 200px;
      object-fit: cover;
      border-radius: 8px;
    }
  
    .product-name {
      font-size: 1.2rem;
      margin: 10px 0;
    }
  
    .product-price {
      font-weight: bold;
      color: green;
    }
  
    .buy-btn, .more-btn {
      background: blue;
      color: white;
      padding: 8px 16px;
      border: none;
      cursor: pointer;
      border-radius: 5px;
      margin: 5px;
    }
  
    .more-btn {
      background: gray;
    }
  </style>
  