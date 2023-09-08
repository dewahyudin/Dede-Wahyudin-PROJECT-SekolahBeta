<template>
  <div>
    <header-component />
    
    <main class="main">
      <h1>Produk Kami</h1>
      <p>Temukan berbagai produk terbaik kami.</p>
      
      <div class="filter-bar">
        <label for="category-filter">Filter Kategori:</label>
        <select id="category-filter" v-model="selectedCategory">
          <option value="">Semua</option>
          <option v-for="category in categories" :key="category">{{ category }}</option>
        </select>
      </div>
      
      <div class="product-list">
        <div v-for="(product, index) in filteredProducts" :key="index" class="product-card">
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
      categories: ['Makanan', 'Minuman', 'Aksesoris'],
      selectedCategory: '',
      products: [
        {
          name: 'Nugget Crispy',
          category: 'Makanan',
          description: 'Nugget Crispy adalah camilan renyah yang terbuat dari daging atau bahan lain yang dilapisi tepung panir dan digoreng',
          price: 'Rp 22.000',
          image: 'https://th.bing.com/th/id/R.4e0a2ebc4ca9db1fb238e4e5651bf23a?rik=tg2Wv0Cf%2bGOaPg&riu=http%3a%2f%2fwww.sickchirpse.com%2fwp-content%2fuploads%2f2018%2f02%2fChicken-Nuggets.jpg&ehk=sqlSnb34rg%2b9jaCgN9G%2fhq4171MAibQM55i5RGEaaX0%3d&risl=&pid=ImgRaw&r=0'
        },
        {
          name: 'Es Dawet',
          category: 'Minuman',
          description: 'Es dawet adalah minuman segar Indonesia dengan dawet hijau, santan, dan gula merah.',
          price: 'Rp 11.000',
          image: 'https://media.suara.com/pictures/970x544/2019/04/08/83173-es-dawet.jpg'
        },
        {
          name: 'Gelang Rajut',
          category: 'Aksesoris',
          description: 'Gelang rajut dibuat handmade dengan bahan berkualitas premium, cocok dipakai buat hangout bareng temen',
          price: 'Rp 7.000',
          image: 'https://i.ytimg.com/vi/CL7YNZvugVc/maxresdefault.jpg'
        },
        
      ]
    }
  },
  computed: {
    filteredProducts() {
      if (!this.selectedCategory) {
        return this.products;
      }
      return this.products.filter(product => product.category === this.selectedCategory);
    }
  }
}
</script>

<style scoped>
/* Gaya CSS untuk halaman produk */
.main {
  max-width: 1200px;
  margin: 0 auto;
  padding: 20px;
}

.filter-bar {
  text-align: center;
  margin-bottom: 20px;
}

.product-list {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
}

.product-card {
  width: calc(33.33% - 20px);
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
