<script setup>
  import Mega_PJ from './MegaMenu/Mega_PJ.vue';
  import Mega_L from './MegaMenu/Mega_L.vue';
  import Mega_R from './MegaMenu/Mega_R.vue';
  import Mega_P from './MegaMenu/Mega_P.vue';
  import Mega_G from './MegaMenu/Mega_G.vue';

  import { ref, Transition } from 'vue';

  const isOpen = ref(false)
  const toggleMenu = () => {
    isOpen.value = !isOpen.value
  }
</script>

<template>
  <header class="header">
    <div class="header_logo">
      <img src="@/assets/logo.png" alt="Logo Biro" class="header_logo-img" />
      <div class="header_title">Biro Pengadaan Barang dan Jasa Sekretariat Daerah</div>
    </div>

    <div @click="toggleMenu" class="nav_menu">
      <img src="@/assets/menu.svg" />
    </div>
      <nav :class="['header_nav', { open: isOpen }]">
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
  box-shadow: 0 6px 14px rgba(0, 0, 0, 0.12);
}

.header_logo {
  display: flex;
  align-items: center;
}

.header_logo-img {
  height: 60px;
  width: auto;
  margin-right: 10px;
}

.header_title {
  font-size: 16px;
  font-weight: bold;
}

.header_nav {
  padding: 1rem;
}

.nav_menu {
  display: none;
  cursor: pointer;
  width: 1%;
  margin-right: 5%;
  background: none;
  border: none;
  color: white;
  font-size: 26px;
  z-index: 10000;
}

.nav_link {
  list-style: none;
  display: flex;
  margin: 0;
  padding: 0;
}
  
.nav_link li {
  margin: 0 10px;
}

.nav_link a {
  transition: color 0.3s ease;
  font-size: 15px;
  text-decoration: none;
  color: #fff;
}

.nav_link a:hover {
  color: #f1c40f;
}

@media (max-width: 768px) {
  
  .nav_menu {
    display: block;
  }

  .header_nav {
    position: fixed;
    top: 0;
    right: 0;
    width: 40%;
    height: 100vh;
    background: #2f6d3f;
    color: white;
    padding: 20px;
    overflow-y: auto;
    z-index: 1000;
    transform: translateX(100%);
    transition: transform 0.3s ease;
  }

  .header_nav.open {
    transform: translateX(0);
  }

  .nav_link {
    flex-direction: column;
    padding: 0;
    margin-top: 50px;
  }

  .nav_link li {
    margin: 10px 0;
  }

  .header_logo-img {
    height: 50px;
    width: 45px;
  }

  .header_title {
    font-size: 14px;
  }
}

</style>