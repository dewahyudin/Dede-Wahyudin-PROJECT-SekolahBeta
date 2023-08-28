<template>
  <div>
    <header-component />
    
    <main class="main">
      <h1>Selamat datang di Toko Online Kami!</h1>
      <p>Temukan produk-produk terbaik untuk Anda.</p>
      
      <div class="product-list">
        <div v-for="(product, index) in products" :key="index" class="product-card">
          <img :src="product.image" :alt="product.name" />
          <h3>{{ product.name }}</h3>
          <p class="description">{{ product.description }}</p>
          <p class="price">{{ product.price }}</p>
        </div>
      </div>
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
        {
          name: 'Produk 1',
          description: 'Deskripsi Produk 1',
          price: 'Rp 100.000',
          image: 'link_gambar_produk_1'
        },
        {
          name: 'Produk 2',
          description: 'Deskripsi Produk 2',
          price: 'Rp 150.000',
          image: 'link_gambar_produk_2'
        },
        // Tambahkan produk lainnya di sini
      ]
    }
  }
}
</script>

<style scoped>
.main {
  max-width: 1200px;
  margin: 0 auto;
  padding: 20px;
}

.product-list {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
  margin-top: 20px;
}

.product-card {
  border: 1px solid #ddd;
  padding: 20px;
  text-align: center;
}

.product-card img {
  max-width: 100%;
  height: auto;
}

.description {
  margin-top: 10px;
  font-size: 14px;
}

.price {
  margin-top: 10px;
  font-weight: bold;
  color: #ff9900;
}
</style>
