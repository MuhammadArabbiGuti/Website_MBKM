<template>
    <div class="page">
    <section class="content-section">
      <div class="content-container">
        <h2>Pelayanan</h2>
        <div class="grid">
          <NuxtLink to="Layanan/standar_p" class="card">
            <h3>Standar Layanan</h3>
            <p>
              Dokumen Berisi Standar Layanan
            </p>
          </NuxtLink>

          <div class="card">
            <h3>Produk / Jenis Pelayanan</h3>
            <p>
              Layanan pengadaan jasa untuk kebutuhan pemerintah
            </p>
          </div>
        </div><br></br>
        <div class="card">
            <h3 style="text-align: center;">Pengisian Formulir</h3>
            <ul>
                <li><NuxtLink to="/layanan/f_MBIZ">Form MBIZ Market</NuxtLink> </li>
                <li><NuxtLink to="/layanan/f_pengaduan">Form Pengaduan</NuxtLink></li>
                <li><NuxtLink to="/layanan/f_pertanyaan">Form Pertanyaan</NuxtLink></li>
                <li><NuxtLink to="/layanan/f_saranusulan">Form Saran dan Usulan</NuxtLink></li>
                <li><NuxtLink to="/layanan/f_permintaan">Form Perminataan Layanan</NuxtLink></li>
                <li><NuxtLink to="/layanan/f_surat">Form Menyampaikan Surat</NuxtLink></li>
            </ul>
        </div>
      </div>
    </section>
    </div>
</template>

<style scoped>
.content-section {
  background-color: #f8f9fa;
  padding: 3rem 1rem;
}
  
.content-container {
  background: white;
  border-radius: 10px;
  padding: 2rem;
  max-width: 1000px;
  margin: 0 auto;
  box-shadow: 0 2px 6px rgba(0, 0, 0, 0.1);
}
  
.content-container h2 {
  margin-bottom: 2rem;
}
  
.grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 1.5rem;
}
  
.card {
  background: #fff;
  border: 1px solid #e5e5e5;
  border-radius: 8px;
  padding: 1.5rem;
  transition: box-shadow 0.2s;
}
  
.card:hover {
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
}
  
.card h3 {
  margin-bottom: 0.8rem;
  color: #2f6d3f;
}
  
.card p, li {
  color: #333;
  font-size: 0.95rem;
  line-height: 1.5;
}

.card ul {
  list-style-type: none;
  text-align: center;
}

.card li {
  font-size: 18px;
  margin-top: 20px;
}

</style>