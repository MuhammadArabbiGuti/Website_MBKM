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
                        <td><a :href="pj.aksi" download class="btn">Download</a></td>
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
    padding: 50px 20px;
    padding-left: 200px;
    padding-right: 400px;
    max-width: 1000px;
    background-color: #f4f6f7;
    align-items: center;
}

.pj_c{
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
