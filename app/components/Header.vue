<script setup>
  import Mega_PJ from './MegaMenu/Mega_PJ.vue';
  import Mega_L from './MegaMenu/Mega_L.vue';
  import Mega_R from './MegaMenu/Mega_R.vue';
  import Mega_P from './MegaMenu/Mega_P.vue';
import Mega_G from './MegaMenu/Mega_G.vue';
</script>

<template>
  <header class="header">
    <div class="header_logo">
      <img src="@/assets/logo.png" alt="Logo Biro" class="header_logo-img" />
      <span class="header_title">Biro Pengadaan Barang dan Jasa Sekretariat Daerah</span>
    </div>
    <nav class="header_nav">
      <ul class="nav_link">
        <li><a href="/">Home</a></li>
        <li><a href="/profile">Profil</a></li>
        <li><Mega_PJ /></li>
        <li><Mega_R /></li>
        <li><Mega_P /></li>
        <li><a href="/Berita/berita">Arsip Berita</a></li>
        <li><Mega_L /></li>
        <li><Mega_G /></li>
        <li><a href="/unduhan">Unduhan</a></li>
        <li><a href="https://pbj.kalbarprov.go.id/ppid/">PPID</a></li>
        <li><a href="/kontak">Kontak</a></li>
      </ul>
    </nav>
  </header>
</template>

<style scoped>

.nav_link {
  list-style: none;
  display: flex;
}
  
.nav_link li {
  position: sticky;
}

.nav_link a {
  transition: color 0.3s ease;
}

.nav_link a:hover {
  color: #f1c40f;
}

.header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  background-color: #2f6d3f;
  padding: 10px 20px;
  color: #fff;
  position: sticky;
  top: 0;
  left: 0;
  z-index: 1000;
}

.header_logo {
  display: flex;
  align-items: center;
}

.header_logo-img {
  height: 70px;
  width: 60px;
  margin-right: 10px;
}

.header_title {
  font-size: 17px;
  font-weight: bold;
}

.header_nav {
  padding: 1rem;
}

.header_nav ul {
  display: flex;
  list-style: none;
  margin: 0;
  padding: 0;
}

.header_nav li {
  margin: 0 10px;
}

.header_nav a {
  text-decoration: none;
  color: #fff;
  font-size: 15px;
}

</style>