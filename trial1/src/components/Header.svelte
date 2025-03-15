<script>
    let isOpen = false; // State for mobile menu
  </script>
  
  <header class="bg-gray-900 text-white shadow-md">
    <div class="container mx-auto flex items-center justify-between p-4">
      <!-- Logo -->
      <a href="/" class="text-2xl font-bold text-blue-400">Phantom Market</a>
  
      <!-- Desktop Nav -->
      <nav class="hidden md:flex space-x-6">
        <a href="#/" class="hover:text-blue-400">Home</a>
        <a href="#/products" class="hover:text-blue-400">Products</a>
        <a href="#/about" class="hover:text-blue-400">About</a>
        <a href="#/contact" class="hover:text-blue-400">Contact</a>
      </nav>
  
      <!-- Mobile Menu Button -->
      <button class="md:hidden focus:outline-none" on:click={() => isOpen = !isOpen}>
        <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7"></path>
        </svg>
      </button>
    </div>
  
    <!-- Mobile Nav -->
    {#if isOpen}
      <nav class="md:hidden bg-gray-800 text-center py-4 space-y-2">
        <a href="#/" class="block text-white hover:text-blue-400">Home</a>
        <a href="#/products" class="block text-white hover:text-blue-400">Products</a>
        <a href="#/about" class="block text-white hover:text-blue-400">About</a>
        <a href="#/contact" class="block text-white hover:text-blue-400">Contact</a>
      </nav>
    {/if}
  </header>
  