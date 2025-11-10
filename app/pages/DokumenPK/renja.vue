<template>
    <section class="rj">
        <div class="rj_c">
            <h2>Dokumen Renja (Rencana Kerja)</h2>
            <table>
                <thead>
                    <tr>
                        <th>No</th>
                        <th>Data</th>
                        <th>Aksi</th>
                    </tr>
                </thead>
                <tbody>
                    <tr v-for="(rj, index) in rjList" :key="index">
                        <td>{{ index + 1 }}</td>
                        <td>{{ rj.nama }}</td>
                        <td><a :href="rj.aksi" download class="btn">Lihat</a></td>
                    </tr>
                </tbody>
            </table>
        </div>
    </section>
</template>

<script setup>
const rjList = [
    {nama:"Rencana Kerja Tahun 2025", aksi: "a"},
    {nama:"Rencana Kerja Tahun 2024", aksi: "a"},
    {nama:"Rencana Kerja Tahun 2023", aksi: "a"},
    {nama:"Rencana Kerja Tahun 2022", aksi: "a"}
]
</script>

<style scoped>
.rj {
    padding: 50px 20px;
    padding-left: 200px;
    padding-right: 400px;
    max-width: 1000px;
    background-color: #f4f6f7;
    align-items: center;
}

.rj_c{
    padding: 20px;
    background: white;
    border-radius: 8px;
    padding: 1.5rem;
    margin-bottom: 2rem;
    box-shadow: 0 2px 6px rgba(0, 0, 0, 0.1);
    margin-left: 200px;
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
