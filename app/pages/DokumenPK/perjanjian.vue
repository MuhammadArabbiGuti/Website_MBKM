<template>
    <section class="pj">
        <div class="pj_c">
            <h2>Perjanjian Kerja</h2>
            <table>
                <thead>
                    <tr>
                        <th>No</th>
                        <th>Dokumen</th>
                        <th>Aksi</th>
                    </tr>
                </thead>
                <tbody>
                    <tr v-for="(pj, index) in pjList" :key="index">
                        <td>{{ index + 1 }}</td>
                        <td>{{ pj.nama }}</td>
                        <td>Download</td>
                    </tr>
                </tbody>
            </table>
        </div>
    </section>
</template>

<script setup>
const pjList = [
    {nama:"PERJANKIN_BIRO_2025", aksi: "a"},
    {nama:"PERJANKIN_KARO_2024_ITKP", aksi: "a"},
    {nama:"PERJANKIN_2024_KASUBBAG_TU", aksi: "a"},
    {nama:"PERJANKIN_2024_KABAG_A", aksi: "a"},
    {nama:"PERJANKIN_2024_KABAG_B", aksi: "a"},
    {nama:"PERJANKIN_2024_KABAG_C", aksi: "a"},
    {nama:"Perjankin Perubahan 2 Karo 2023", aksi: "a"},
    {nama:"PERJANKIN PERUBAHAN 2 KASUBBAG TU", aksi: "a"},
    {nama:"PERJANKIN PERUBAHAN 2 KABAG A", aksi: "a"},
    {nama:"PERJANKIN PERUBAHAN 2 KABAG B", aksi: "a"},
    {nama:"PERJANKIN PERUBAHAN 2 KABAG C", aksi: "a"},
    {nama:"PERJANKIN-2021", aksi: "a"},
    {nama:"PERJANKIN-2020", aksi: "a"}
]
</script>

<style scoped>
.pj {
    width: 100%;
    max-width: 2000px;
    background-color: #f4f6f7;
    align-items: center;
    padding: 20px 0;
}

.pj_c{
    padding: 20px;
    background: white;
    border-radius: 8px;
    margin: 0 200px;
    box-shadow: 0 2px 6px rgba(0, 0, 0, 0.1);
    overflow-x: auto;
}

.pj_c h2 {
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
    .pj_c {
        margin: 10px
    }
}

</style>
