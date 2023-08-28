<!-- pages/kontak.vue -->
<template>
    <div>
      <header-component />
      
      <main class="main">
        <h1>Hubungi Kami</h1>
        <p>Untuk informasi lebih lanjut, silakan hubungi kami di dwahyudin568@gmail.com.</p>
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
    }
  }
  </script>
  