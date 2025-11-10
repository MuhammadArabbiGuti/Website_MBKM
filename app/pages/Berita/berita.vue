<script setup>
import { ref, computed } from "vue"

const berita = ref([
  { id: 1, judul: "Pengadaan Barang Tahap I", tanggal: "2025-01-15" },
  { id: 2, judul: "Pengadaan Jasa Tahap II", tanggal: "2025-02-05" },
  { id: 3, judul: "Laporan Akhir Tahun", tanggal: "2025-12-20" },
  { id: 4, judul: "Evaluasi Semester Pertama", tanggal: "2025-06-30" }
])

const bulanTahun = [
  "Januari 2025", "Februari 2025", "Maret 2025",
  "April 2025", "Mei 2025", "Juni 2025",
  "Juli 2025", "Agustus 2025", "September 2025",
  "Oktober 2025", "November 2025", "Desember 2025"
]

const selectedFilter = ref("")

const filteredBerita = computed(() => {
  if (!selectedFilter.value) return berita.value

  const [bulanNama, tahun] = selectedFilter.value.split(" ")

  const bulanMap = {
    Januari: "01", Februari: "02", Maret: "03", April: "04",
    Mei: "05", Juni: "06", Juli: "07", Agustus: "08",
    September: "09", Oktober: "10", November: "11", Desember: "12"
  }

  const bulan = bulanMap[bulanNama]

  return berita.value.filter(item => {
    return item.tanggal.startsWith(`${tahun}-${bulan}`)
  })
})
</script>

<template>
  <div class="berita-list">
    <h2>Arsip Berita</h2>

    <div class="filter">
      <label for="filter">Filter berdasarkan bulan dan tahun:</label>
      <select id="filter" v-model="selectedFilter">
        <option value="" selected>Semua</option>
        <option v-for="item in bulanTahun" :key="item" :value="item">
          {{ item }}
        </option>
      </select>
    </div>

    <div class="berita-daftar">
    <ul>
      <li v-for="item in filteredBerita" :key="item.id" class="berita-item">
        <NuxtLink :to="`/berita/${item.id}`">
          {{ item.judul }} ({{ item.tanggal }})
        </NuxtLink>
      </li>
    </ul>
  </div>
  </div>
</template>

<style scoped>

.berita-list {
  padding: 20px;
  max-width: 800px;
  margin: 2rem auto;
  background: #fff;
  padding: 2rem;
  border-radius: 8px;
  box-shadow: 0 2px 6px rgba(0,0,0,0.1);
}

.berita-daftar ul {
  list-style: none;
  padding: 0;
}

.berita-daftar li {
  margin: 8px 0;
}

.berita-daftar a {
  text-decoration: none;
  color: #0077cc;
}

.berita-daftar a:hover {
  text-decoration: underline;
}

.filter {
  margin-bottom: 15px;
}

select {
  margin-left: 10px;
  padding: 5px;
  margin-left: 0.5rem;
  padding: 0.5rem;
  border-radius: 6px;
  border: 1px solid #ccc;
}

.berita-daftar {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.berita-item {
  padding: 20px;
  max-width: 800px;
  margin: 2rem auto;
  background: #fff;
  padding: 2rem;
  border-radius: 8px;
  box-shadow: 0 2px 6px rgba(0,0,0,0.1);
}

.tanggal {
  font-size: 0.9rem;
  color: #666;
}
</style>