<template>
  <header class="header">
    <nav class="nav">
      <div class="logo">KampusMart</div>
      <ul class="menu">
        <li><a href="/">Beranda</a></li>
        <li><a href="/produk">Produk</a></li>
        <li><a href="/kontak">Kontak</a></li>
      </ul>
    </nav>
  </header>
</template>

<style scoped>
.header {
  background-color: #333;
  color: white;
  padding: 10px 0;
}

.nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  max-width: 1200px;
  margin: 0 auto;
}

.logo {
  font-size: 24px;
  font-weight: bold;
}

.menu {
  list-style: none;
  display: flex;
}

.menu li {
  margin-right: 20px;
}

.menu a {
  color: white;
  text-decoration: none;
  font-weight: bold;
}

.menu a:hover {
  color: #ff9900;
}
</style>
