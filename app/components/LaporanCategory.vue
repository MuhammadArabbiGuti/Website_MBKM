<script setup>
  import LaporanCard from './LaporanCard.vue';
</script>

<template>
    <section class="report-category">
      <div class="container">
        <h2 class="section-title">Kategori Laporan</h2>
        <div class="grid">
          <a href="/Laporan/pengaduan"><LaporanCard
            title="Laporan Pengaduan"
          /></a>
          <a href="/Laporan/l_kinerja"><LaporanCard
            title="Laporan Kinerja"
          /></a>
          <a href="/Laporan/r_pengadaan"><LaporanCard
            title="Realisasi Pengadaan"
          /></a>
          <a href="/Laporan/lm_resiko"><LaporanCard
            title="Laporan Manajemen Resiko"
          /></a>
          <a href="/Laporan/l_keuangan"><LaporanCard
            title="Laporan Keuangan"
          /></a>
          <a href="/Laporan/lm_evaluasi"><LaporanCard
            title="Laporan Monitoring dan Evaluasi"
          /></a>
          <a href="/Laporan/skm"><LaporanCard
            title="Survey Kepuasan Masyarakat"
          /></a>
          <a href="https://forms.gle/6A4HsC2wyxEU2soh7" target="_blank"><LaporanCard
            title="SKM (EKSTERNAL)"
          /></a>
          <a href="https://forms.gle/aDZUDsdosQcsBL5m7" target="_blank"><LaporanCard
            title="SKM (INTERNAL)"
          /></a>
        </div>
      </div>
    </section>
</template>
  
<style scoped>
  
.report-category {
  background: #f8fafc;
  padding: 40px 20px;
}
  
.section-title {
  font-size: 28px;
  font-weight: bold;
  margin-bottom: 30px;
}
  
.grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 20px;
}

</style>
  