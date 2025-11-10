<template>
    <section class="about">
      <div class="about_container">
        <div class="about_content">
          <h2 class="about_title">Sejarah Biro</h2>
          <p class="about_history">
            Sejarah Terbentuknya UKPBJ Provinsi KALBAR Biro Pengadaan Barang/Jasa adalah, 
            Pergub Nomor 24 Tahun 2015, Pergub Nomor 69 Tahun 2016, Pergub Nomor 95 Tahun 2018, 
            Pergub Nomor 77 Tahun 2019.
          </p>
        </div>
        <br></br>
        <div class="about_image">
          <img src="/assets/sejarah.png" alt="Tentang Biro" />
        </div>
        <div class="about_image">
          <img src="/assets/zona-integritas.jpg" alt="Zona Integritas" />
        </div>
      </div>
    </section>
</template>
  
<style scoped>

.about {
  padding: 80px 20px;
  background-color: #f4f6f7;
}
  
.about_container {
  max-width: 1200px;
  margin: 0 auto;
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 40px;
  align-items: center;
}
  
.about_title {
  font-size: 28px;
  font-weight: bold;
  color: #2f6d3f;; 
  margin-bottom: 20px;
}
  
.about_history {
  font-size: 16px;
  line-height: 1.6;
  color: #2c3e50;
  margin-bottom: 30px;
}
  
.about_image img {
  width: 90%;
  border-radius: 8px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
} 
  
@media (max-width: 992px) {
  .about_container {
    grid-template-columns: 1fr;
    text-align: center;
  }
  
  .about_content {
    order: 2;
  }
  
  .about_image {
    order: 1;
  }
}

</style>
  