<template>
    <section class="hero">
      <div class="hero_content">
        <h1 class="hero_title">
          Biro Pengadaan Barang dan Jasa<br />
          Sekretariat Daerah Kalimantan Barat
        </h1>
        <p class="hero_subtitle">
          Mewujudkan pengadaan yang efisien, terbuka, dan terpercaya.
        </p>
      </div>
    </section>
</template>
  
  
<style scoped>
  
.hero {
  background-color: #2f6d3f;
  color: #fff;
  padding: 80px 20px;
  text-align: center;
  background-image: url("@/assets/kantor.jpg");
  background-size: cover;
  background-position: center;
  position: relative;
}
  
.hero::after {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(10, 109, 54, 0.8);
}
  
.hero_content {
  position: relative;
  z-index: 1;
  max-width: 900px;
  margin: 0 auto;
}
  
.hero_title {
  font-size: 40px;
  font-weight: bold;
  margin-bottom: 20px;
  line-height: 1.3;
}
  
.hero_subtitle {
  font-size: 18px;
  margin-bottom: 30px;
}
  
</style>
  