<template>
    <section class="pimpinan">
      <div class="pimpinan_container">
        <div class="pimpinan_photo">
          <h2>Profil Pimpinan</h2>
          <img src="@/assets/pimpinan-biro.png" alt="Kepala Biro" />
        </div>
        <div class="pimpinan_info">
          <h2>Kepala Biro Pengadaan Barang dan Jasa</h2>
          <h3>Drs. Aswin Khatib, M.Si</h3>
          <p>
            (Quotes)
          </p>
        </div>
      </div>
    </section>
</template>
  
<style scoped>

.pimpinan {
  padding: 80px 20px;
  background-color: #f4f6f7;
}
  
.pimpinan_container {
  max-width: 1000px;
  margin: 0 auto;
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  gap: 40px;
}
  
.pimpinan_photo img {
  width: 250px;
  height: 300px;
  object-fit: cover;
  border-radius: 8px;
  border: 4px solid #1b4332;
  box-shadow: 0 4px 12px rgba(0,0,0,0.1);
}

.pimpinan_photo h2 {
  margin-bottom: 30px;
}
  
.pimpinan_info {
  flex: 1;
}
  
.pimpinan_info h2 {
  font-size: 22px;
  font-weight: 600;
  color: #2f6d3f;
  margin-bottom: 10px;
}
  
.pimpinan_info h3 {
  font-size: 20px;
  font-weight: 700;
  color: #1b4332;
  margin-bottom: 15px;
}
  
.pimpinan_info p {
  font-size: 16px;
  line-height: 1.6;
  color: #333;
}

</style>
  