<template>
  <section class="t">
    <div class="t_c">
      <h2>SOP Bagian Pembinaan dan Advokasi</h2>

      <div v-if="pending">Loading...</div>
      <div v-else-if="error">Gagal mengambil data</div>

      <table v-else>
        <thead>
          <tr>
            <th>No</th>
            <th>Nama File</th>
            <th>Format File</th>
            <th>Aksi</th>
          </tr>
        </thead>

        <tbody>
          <tr v-for="(sop, index) in sopList" :key="index">
            <td>{{ index + 1 }}</td>
            <td>{{ sop.nama }}</td>
            <td>{{ sop.format }}</td>
            <td>
              <a 
                :href="sop.aksi"
                target="_blank"
                download
              >
                Download
              </a>
            </td>
          </tr>
        </tbody>
      </table>

    </div>
  </section>
</template>
  
<script setup>
import { computed } from "vue"

const { data, pending, error } = await useFetch(
  "https://awdiv2.kalbarprov.go.id/api/contents/pbj.kalbarprov.go.id/sop-pa"
)

const extractFiles = (html) => {
  const regex = /href="([^"]+)"[^>]*>(.*?)<\/a>/gi
  let result = []
  let match

  while ((match = regex.exec(html)) !== null) {
    result.push({
      url: match[1],
      nama: match[2]
    })
  }

  return result
}

const getFormat = (url) => {
  if (!url) return "-"

  if (url.toLowerCase().includes(".pdf")) return "PDF"
  if (url.toLowerCase().includes(".docx")) return "DOCX"
  if (url.toLowerCase().includes(".xlsx")) return "XLSX"

  return "-"
}

const sopList = computed(() => {
  const items = data.value?.data || []

  let hasil = []

  items.forEach(item => {
    const files = extractFiles(item.content)

    files.forEach(file => {
      hasil.push({
        nama: file.nama,
        format: getFormat(file.url),
        aksi: file.url
      })
    })
  })

  return hasil
})
</script>

<style scoped>

.t {
  width: 100%;
  max-width: 2000px;
  background-color: #f4f6f7;
  align-items: center;
  padding: 20px 0;
}

.t_c{
  padding: 20px;
  background: white;
  border-radius: 8px;
  margin: 0 200px;
  box-shadow: 0 2px 6px rgba(0, 0, 0, 0.1);
  overflow-x: auto;
}

.t_c h2 {
  border-bottom: 2px solid #f1c40f;
  padding-bottom: 2%;
}

table {
  width: 100%;
  border-collapse: collapse;
  margin-top: 10px;
  min-width: 600px;
}

th, td {
  border: none;
  padding: 8px;
  text-align: left;
}

th {
  background-color: #2f6d3f;
  color: white;
}

a {
  padding: 5px;
  transition: background-color 0.3s ease;
  border-radius: 10px;
}

a:hover {
  text-decoration: none;
  background-color: #f1c40f;
  color: #fff;
}

@media (max-width: 768px) {
    .t_c {
        margin: 10px
    }
}

</style>