<script setup>
import { ref, computed } from "vue"

const bulanTahun = computed(() => {
  const map = {
    "01": "Januari", "02": "Februari", "03": "Maret",
    "04": "April", "05": "Mei", "06": "Juni",
    "07": "Juli", "08": "Agustus", "09": "September",
    "10": "Oktober", "11": "November", "12": "Desember"
  }

  const list = []

  berita.value.forEach(item => {
    if (!item.date) return

    const [tahun, bulan] = item.date.split("-")

    list.push({
      label: `${map[bulan]} ${tahun}`,
      value: `${tahun}-${bulan}`
    })
  })

  // hapus duplikat
  const unik = Array.from(
    new Map(list.map(item => [item.value, item])).values()
  )

  // urutkan terbaru dulu
  return unik.sort((a, b) => b.value.localeCompare(a.value))
})

const selectedFilter = ref("")

const { data, pending, error } = await useFetch(
  "https://awdiv2.kalbarprov.go.id/api/site_articles/pbj.kalbarprov.go.id"
)

const berita = computed(() => {
  return data.value?.data?.data || []
})

const filteredBerita = computed(() => {
  if (!selectedFilter.value) return berita.value

  return berita.value.filter(item => {
    return item.date?.startsWith(selectedFilter.value)
  })
})
</script>

<template>
  <div class="berita-list">
    <h2>Arsip Berita</h2>

    <div class="filter">
      <label for="filter">Filter berdasarkan bulan dan tahun:</label>
      <select v-model="selectedFilter">
        <option value="">Semua</option>

        <option 
          v-for="item in bulanTahun" 
          :key="item.value" 
          :value="item.value"
        >
          {{ item.label }}
        </option>
      </select>
    </div>

    <div class="berita-daftar">
    <ul>
      <li v-for="item in filteredBerita" :key="item.id" class="berita-item">
        <div class="item">
        <NuxtLink :to="`/berita/${item.id}`">
          {{ item.title }}
        </NuxtLink>
        </div>
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