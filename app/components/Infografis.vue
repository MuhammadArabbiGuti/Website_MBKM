<template>
    <section class="t">
      <h2>Infografis</h2>
    <div class="table-container">
      <table>
        <thead>
          <tr>
            <th>No</th>
            <th>Nama File</th>
            <th>Format File</th>
            <th>Ukuran File</th>	
            <th>Aksi</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="(laporan, index) in laporanList" :key="index">
            <td>{{ index + 1 }}</td>
            <td>{{ laporan.nama }}</td>
            <td>{{ laporan.format }}</td>
            <td>{{ laporan.ukuran }}</td>
            <td>
            <td
              v-if="laporan.format === 'Youtube'" 
              :href="laporan.aksi" 
              target="_blank"> Tonton </td>
            <td
             v-else-if="laporan.format === 'PDF'"
              > Donwload </td>
            </td>
          </tr>
        </tbody>
      </table>
    </div>
    </section>
  </template>
  
  <script setup>
  const laporanList = [
    { nama: "Buku Panduan Pengisian e-Kontrak", format: "PDF", ukuran: "3.6 MB",	aksi: "Download"},
    { nama: "Sosialisasi Melalui Video Proses Pengisian e-Kontrak", format: "Youtube", ukuran: "-", aksi: "https://youtu.be/BcNdevqiKoQ"},
    { nama: "Buku Sosialisasi e-Katalog Lokal", format: "PDF", ukuran: "1.6 MB", aksi: "Download"},
    { nama: "Buku Sosialisasi e-Pengadaan Langsung", format: "PDF", ukuran: "1.19 MB",	aksi: "Download"}
  ]
  </script>

<style scoped>

.t {
  width: 100%;
  max-width: 2000px;
  background-color: #f4f6f7;
  align-items: center;
  padding-top: 20px;
  padding-bottom: 20px;
}

.table-container {
  padding: 20px;
  background: white;
  border-radius: 8px;
  margin: 20px;
  box-shadow: 0 2px 6px rgba(0, 0, 0, 0.1);
  overflow-x: auto;
}

.t h2{
  margin: 20px 20px;
  border-bottom: 2px solid #f1c40f;
  padding-bottom: 1%;
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

</style>