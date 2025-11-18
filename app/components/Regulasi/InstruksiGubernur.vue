<template>
    <section class="t">
    <div class="t_c">
      <h2>Instruksi Gubernur</h2>
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