<template>
    <section class="t">
      <h2>Instruksi Gubernur</h2>
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
            <td><a :href="laporan.aksi" download>Download</a></td>
          </tr>
        </tbody>
      </table>
    </div>
    </section>
</template>
  
  <script setup>
  const laporanList = [
    { nama: "Instruksi Gubernur", format: "PDF", ukuran: "656.67 KB",	aksi: "Download"},
    { nama: "Instruksi Gubernur Percepatan Penyelenggaraan Katalog Elektrnonik", format: "PDF", ukuran: "430.26 KB",	aksi: "Download"}
  ]
  </script>

<style scoped>

.t {
  width: 1500px;
  background-color: #f4f6f7;
  align-items: center;
  padding-top: 20px;
  padding-bottom: 20px;
  padding-right: 20px;
}

.table-container {
  padding: 20px;
  background: white;
  border-radius: 8px;
  padding: 1.5rem;
  margin-bottom: 2rem;
  box-shadow: 0 2px 6px rgba(0, 0, 0, 0.1);
  margin-left: 20px;
  margin-top: 20px;
}

.t h2{
  margin: 20px 20px;
}

table {
  width: 100%;
  border-collapse: collapse;
  margin-top: 10px;
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