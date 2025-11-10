<template>
    <section class="layanan-utama">
      <div class="layanan-utama_container">
        <h2 class="layanan-utama_title">AKSIPRAJA</h2>
        <p>Aplikasi Pengadaan Barang dan Jasa, dikembangkan oleh Biro Pengadaan Barang dan
           Jasa Sekretariat Daerah Provinsi Kalimantan Barat sejak Tahun 2017 dan merupakan
            Best Practice dari Penyelenggaraan Pengadaan Barang dan Jasa di Provinsi Kalimantan Barat.</p>
        <div class="layanan-utama_grid">
          <NuxtLink to="https://sipraja.kalbarprov.go.id/login" class="layanan-card" target="_blank">
            <div class="icon"><img src="assets/logo.png"></img></div>
            <h3>SIPRAJA</h3>
            <p>Sistem Informasi Persiapan Pengadaan Barang / Jasa.</p>
          </NuxtLink>

          <NuxtLink to="https://lpse.kalbarprov.go.id/eproc4" class="layanan-card" target="_blank">
            <div class="icon"><img src="assets/SPSE.svg"></img></div>
            <h3>SPSE</h3>
            <p>Sistem Pengadaan Secara Elektronik.</p>
          </NuxtLink>
  
          <NuxtLink to="https://sip-spse.kalbarprov.go.id/" class="layanan-card" target="_blank">
            <div class="icon"><img src="assets/sip-spse.png"></img></div>
            <h3>DASHBOARD PBJ</h3>
            <p>Alat bantu untuk mempermudah para pelaku pengadaan..</p>
          </NuxtLink>
  
          <NuxtLink to="https://www.lapor.go.id/" class="layanan-card" target="_blank">
            <div class="icon"><img src="assets/lapor.jpg"></img></div>
            <h3>LAPOR!</h3>
            <p>Layanan Aspirasi dan Pengaduan Online Rakyat.</p>
          </NuxtLink>
        </div>
      </div>
    </section>
</template>
  
<style scoped>

.layanan-utama {
  padding: 80px 20px;
  background-color: #ffffff;
}

.layanan-utama_container {
  max-width: 1200px;
  margin: 0 auto;
  text-align: center;
}
  
.layanan-utama_title {
  font-size: 28px;
  font-weight: bold;
  color: #0a6d36; 
  margin-bottom: 40px;
}
  
.layanan-utama_grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
  gap: 30px;
}
  
.layanan-card {
  background: #f4f6f7; 
  border-radius: 8px;
  padding: 30px 20px;
  text-align: center;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}
  
.layanan-card:hover {
  transform: translateY(-6px);
  box-shadow: 0 6px 14px rgba(0, 0, 0, 0.12);
  text-decoration: none;
}
  
.icon {
  font-size: 32px;
  background-color: #f4f6f7; 
  color: #000;
  width: 100px;
  height: 100px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  margin: 0 auto 20px auto;
}

.icon img {
  width: 80px;
}
  
.layanan-card h3 {
  font-size: 20px;
  font-weight: bold;
  margin-bottom: 10px;
  color: #0a6d36;
}
  
.layanan-card p {
  font-size: 15px;
  color: #2c3e50;
  line-height: 1.5;
}

.layanan-utama_container p {
  font-size: 20px;
  color: #2c3e50;
  line-height: 1.5;
  margin-bottom: 50px;
}

</style>
  