<!-- pages/produk.vue -->
<template>
    <div>
      <header-component />
      
      <main class="main">
        <h1>Daftar Produk</h1>
        <ul>
          <li v-for="(product, index) in products" :key="index">{{ product.name }}</li>
        </ul>
      </main>
      
      <footer-component />
    </div>
  </template>
  
  <script>
  import HeaderComponent from '@/components/Header.vue'
  import FooterComponent from '@/components/Footer.vue'
  
  export default {
    components: {
      HeaderComponent,
      FooterComponent
    },
    data() {
      return {
        products: [
          { name: 'Sosis' },
          { name: 'Nugget' },
          // Tambahkan produk lainnya di sini
        ]
      }
    }
  }
  </script>
  