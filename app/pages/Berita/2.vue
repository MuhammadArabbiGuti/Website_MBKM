<script setup>
import { useRoute } from "vue-router"
import { ref } from "vue"

const route = useRoute()

const berita = ref([
  { id: 1, judul: "Pengadaan Barang Tahap I", tanggal: "2025-01-15" },
  { id: 2, judul: "Pengadaan Jasa Tahap II", tanggal: "2025-02-05" },
  { id: 3, judul: "Laporan Akhir Tahun", tanggal: "2025-12-20" },
  { id: 4, judul: "Evaluasi Semester Pertama", tanggal: "2025-06-30" }
])

const detail = berita.value.find(item => item.id === Number(route.params.id))
</script>

<template>
  <div class="berita-detail">
    <NuxtLink to="/Berita/berita">← Kembali</NuxtLink>

    <h3> (Isi berita 2)</h3>
    <img src="/assets/kantor.jpg"></img>

  </div>
</template>

<style scoped>

.berita-detail {
  padding: 20px;
}

.berita-detail img{
  max-width: 500px;
  border-radius: 6px;
  margin: 1rem 0;
}

</style>
