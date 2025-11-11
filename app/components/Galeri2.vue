<template>
    <div class="gallery-page">
    <header class="gallery-header">
      <h1>Galeri Pelayanan</h1>
      <p>Dokumentasi Standar Pelayanan biro pengadaan barang dan jasa</p>
    </header>

    <section class="gallery-grid">
      <img src="/assets/layanan1a.png" alt="Foto Pelayanan 1" class="gallery-item">      
      <img src="/assets/layanan1b.png" alt="Foto Pelayanan 2" class="gallery-item">            
      <img src="/assets/layanan2a.png" alt="Foto Pelayanan 3" class="gallery-item">           
      <img src="/assets/layanan2b.png" alt="Foto Pelayanan 4" class="gallery-item">           
      <img src="/assets/layanan3a.png" alt="Foto Pelayanan 5" class="gallery-item">          
      <img src="/assets/layanan3b.png" alt="Foto Pelayanan 6" class="gallery-item">     
    </section>
  </div>

</template>

<style scoped>
.gallery-page {
  padding: 2rem;
  background: #f9f9f9;
}

.gallery-header {
  text-align: center;
  margin-bottom: 2rem;
}

.gallery-header h1 {
  font-size: 2rem;
  color: #064e3b;
}

.gallery-header p {
  color: #444;
  font-size: 1rem;
}

.gallery-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
}

.gallery-item {
  background: white;
  border-radius: 8px;
  box-shadow: 0 2px 6px rgba(0,0,0,0.1);
  transition: transform 0.3s ease;
  align-items: center;
  margin-left: 140px;
  margin-bottom: 20px;
  width: auto;
  height: 600px;
}

.gallery-item:hover {
  transform: scale(1.1);
}

</style>