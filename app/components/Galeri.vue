<template>
    <div class="gallery-page">
    <header class="gallery-header">
      <h1>Galeri</h1>
      <p>Dokumentasi foto dan video kegiatan pengadaan barang dan jasa pemerintah</p>
    </header>

    <h2>Galeri Foto</h2>
    <section class="gallery-grid">
      <div class="gallery-item">
        <img src="/assets/kantor.jpg" alt="Foto Kegiatan 1">
      </div>
      <div class="gallery-item">
        <img src="/assets/kantor.jpg" alt="Foto Kegiatan 2">
      </div>
      <div class="gallery-item">
        <img src="/assets/kantor.jpg" alt="Foto Kegiatan 3">
      </div>
      <div class="gallery-item">
        <img src="/assets/kantor.jpg" alt="Foto Kegiatan 1">
      </div>
      <div class="gallery-item">
        <img src="/assets/kantor.jpg" alt="Foto Kegiatan 2">
      </div>
      <div class="gallery-item">
        <img src="/assets/kantor.jpg" alt="Foto Kegiatan 3">
      </div>
    </section>
    <br></br>
    
    <h2>Galeri Video</h2>
    <section class="gallery-grid">
      <div class="gallery-item video">
        <iframe width="100%" height="200" 
          src="https://www.youtube.com/embed/ScMzIvxBSi4" 
          title="YouTube video player" 
          frameborder="0" 
          allowfullscreen>
        </iframe>
      </div>
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
  grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
  gap: 1.5rem;
}

.gallery-item {
  background: white;
  border-radius: 8px;
  overflow: hidden;
  box-shadow: 0 2px 6px rgba(0,0,0,0.1);
  transition: transform 0.3s ease;
}

.gallery-item img {
  width: 100%;
  height: 200px;
  object-fit: cover;
}

.gallery-item:hover {
  transform: scale(1.1);
}

</style>