<template>
  <div>
    <header-component />
    
    <main class="main">
      <h1>Hubungi Kami</h1>
      <p>Silakan hubungi kami melalui informasi kontak berikut:</p>
      
      <ul class="contact-list">
        <li>Email: kampusmart@example.com</li>
        <li>Telepon: (123) 456-7890</li>
        <li>Alamat: Jl. Purnawarman</li>
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
}
</script>

<style scoped>
</style>
