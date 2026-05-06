<template>
    <section class="ind">
        <div class="ind_c">
            <h2>Indikator Kinerja Utama</h2>
            <table>
                <thead>
                    <tr>
                        <th>No</th>
                        <th>Dokumen</th>
                        <th>Aksi</th>
                    </tr>
                </thead>
                <tbody>
                    <tr v-for="(ind, index) in indList" :key="index">
                        <td>{{ index + 1 }}</td>
                        <td>{{ ind.nama }}</td>
                        <td>Download</td>
                    </tr>
                </tbody>
            </table>
        </div>
    </section>
</template>

<script setup>
const indList = [
    {nama:"INDIKATOR KINERJA INDIVIDU 2025", aksi: "a"},
    {nama:"INDIKATOR KINERJA INDIVIDU 2024", aksi: "a"},
    {nama:"IKU-2021", aksi: "a"},
    {nama:"IKU-2020", aksi: "a"}
]
</script>

<style scoped>
.ind {
    width: 100%;
    max-width: 2000px;
    background-color: #f4f6f7;
    align-items: center;
    padding: 20px 0;
}

.ind_c{
    padding: 20px;
    background: white;
    border-radius: 8px;
    margin: 0 200px;
    box-shadow: 0 2px 6px rgba(0, 0, 0, 0.1);
    overflow-x: auto;
}

.ind_c h2 {
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
    .ind_c {
        margin: 10px
    }
}

</style>
