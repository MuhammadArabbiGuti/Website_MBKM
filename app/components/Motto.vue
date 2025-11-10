<template>
    <section class="motto">
      <div class="motto_container">
        <div class="motto_text">
          <h2>Motto</h2>
          <h2>“SKOPER”</h2>
          <p class="motto_quote">
            "STRATEGIS, KOLABORATIF, BERORIENTASI PADA KINERJA, PROAKTIF, dan PERBAIKAN BERKELANJUTAN"
          </p>
          <ul class="motto_list">
            <li>S (STRATEGIS):
                <p>Mewujudkan fungsi pengadaan yang memainkan peran penting dalam mencapai tujuan organisasi
                    melalui perencanaan dan eksekusi anggaran serta pengelolaan sumber daya yang efektif.
                </p>
            </li>
            <li>K (KOLABORATIF):
                <p>Memupuk kolaborasi dan sinergi diantara pemangku kepentingan untuk kinerja fungsi pengadaan
                    yang optimal.
                </p>
            </li>
            <li>O (ORIENTASI KERJA):
                <p>
                    Membangun budaya berbasis kinerja dalam fungsi pengadaan untuk meningkatkan nilai tambah di
                    4 area (waktu proses, biaya, kualitas dan tingkat layanan pengadaan).
                </p>
            </li>
            <li>P (PROAKTIF):
                <p>
                    Menciptakan pergeseran paradigma dalam rantai pengadaan barang dan jasa yang berorientasi
                    pada pelanggan.
                </p>
            </li>
            <li>Per (PERBAIKAN BERKELANJUTAN):
                <p>
                    Secara berkelanjutan meningkatkan kapabilitas organisasi pengadaan sebagai organisasi pembelajaran
                    dengan mengadopsi praktik terbaik pengadaan.
                </p>
            </li>
          </ul>
        </div>
        <div class="motto_photo">
          <img src="@/assets/motto.jpg" alt="Motto Biro" />
        </div>
      </div>
    </section>
</template>
  
<style scoped>

.motto {
  padding: 60px 20px;
  background-color: #ffffff;
}
  
.motto_container {
  max-width: 1000px;
  margin: 0 auto;
  display: flex;
  flex-wrap: wrap;
  align-items: left;
  gap: 40px;
}

.motto_text {
  flex: 1;
}
  
.motto_text h2 {
  font-size: 30px;
  font-weight: 700;
  color: #1b4332; 
  margin-bottom: 10px;
}

.motto_list {
  font-size: 24px;
  font-weight: 700;
  color: #1b4332; 
  margin-bottom: 10px;
}

.motto_list p {
  font-size: 16px;
  line-height: 1.6;
  color: #333;
}
  
.motto_quote {
  font-size: 20px;
  font-style: italic;
  color: #2d6a4f; 
  border-left: 4px solid #f1c40f; 
  padding-left: 12px;
}
  
.motto_photo img {
  margin-top: 20%;
  width: 350px;
  height: auto;
  border-radius: 8px;
  object-fit: cover;
  box-shadow: 0 4px 12px rgba(0,0,0,0.1);
}

</style>
  