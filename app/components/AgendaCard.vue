<script setup>
import { computed } from "vue"

// ambil data dari API
const { data, pending, error } = await useFetch(
    "https://awdiv2.kalbarprov.go.id/api/agenda?site=pbj.kalbarprov.go.id"
)

// mapping data
const agendaList = computed(() => {
  return data.value?.data?.map(item => {
    const tanggal = new Date(item.start)

    return {
      hari: tanggal.toLocaleDateString("id-ID", { weekday: "long" }),
      tanggal: tanggal.toLocaleDateString("id-ID"),
      lokasi: item.location || "-",
      waktu_mulai: item.start?.substring(11, 16) || "-",
      waktu_selesai: item.end?.substring(11, 16) || "-",
      judul: item.title
    }
  }) || []
})
</script>

<template>
  <section class="agenda-section">
    <h2>Agenda</h2>

    <!-- loading -->
    <div v-if="pending">Memuat agenda...</div>

    <!-- error -->
    <div v-else-if="error">Gagal memuat agenda</div>

    <div v-else-if="agendaList.length === 0" class="no-data">Tidak ada agenda</div>

    <!-- data -->
    <div v-else class="agenda-container">
      <div
        v-for="(item, index) in agendaList"
        :key="index"
        class="agenda-card"
      >
        <h3>{{ item.hari }}</h3>
        <p class="tanggal">{{ item.tanggal }}</p>
        <p> {{ item.lokasi }}</p>
        <p> {{ item.waktu_mulai }} - {{ item.waktu_selesai }}</p>
        <p class="judul">{{ item.judul }}</p>
      </div>
    </div>
  </section>
</template>

<style scoped>
.agenda-section {
  padding: 10px 20px;
  background-color: #f4f6f7;
  text-align: center;
}

.agenda-section h2 {
  font-size: 28px;
  font-weight: bold;
  color: #2f6d3f; 
  margin-bottom: 40px;
  border-bottom: solid #f1c40f 2px;
  padding-bottom: 1%;
}

.agenda-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 20px;
  margin-bottom: 20px;
}

.agenda-card {
  background: #ffffff;
  color: #2c3e50;
  padding: 20px;
  border-radius: 12px;
  width: 280px;
  text-align: left;
  border: solid #f1c40f 1px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.06);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.agenda-card p {
    color: black;
}

.tanggal {
  font-size: 0.9rem;
  color: #ccc;
}

.judul {
  margin-top: 10px;
  font-weight: bold;
}

.no-data {
  font-size: 20px;
  font-weight: bold;
  color: #2f6d3f; 
  padding-bottom: 20px;
}
</style>