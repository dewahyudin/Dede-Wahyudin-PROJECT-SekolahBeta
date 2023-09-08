<template>
  <div>
    <header-component />
    
    <main class="main" style="background-image: url('https://wallpapercave.com/wp/wp3376127.jpg');">
      <section class="store-info">
        <h1>Selamat datang di KampusMart</h1>
        <p>Temukan berbagai produk terbaik kami.</p>
        <router-link to="/produk">
          <button class="btn">Lihat Produk</button>
        </router-link>
      </section>
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
/* Gaya CSS untuk halaman beranda */
.main {
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  height: 80vh;
  display: flex;
  justify-content: center;
  align-items: center;
  color: white;
  text-align: center;
}

.store-info {
  background-color: rgba(0, 0, 0, 0.5); /* Latar belakang transparan untuk teks */
  padding: 20px;
  border-radius: 10px;
}

.store-info h1 {
  font-size: 36px;
  margin: 0;
}

.store-info p {
  font-size: 18px;
  margin: 0;
}

.btn {
  background-color: #ff9900;
  color: white;
  padding: 10px 20px;
  border: none;
  border-radius: 5px;
  font-size: 18px;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

.btn:hover {
  background-color: #ff6600;
}
</style>
