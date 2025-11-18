<template>
    <section class="ra">
        <div class="ra_c">
            <h2>Rencana Aksi</h2>
            <table>
                <thead>
                    <tr>
                        <th>No</th>
                        <th>Data</th>
                        <th>Aksi</th>
                    </tr>
                </thead>
                <tbody>
                    <tr v-for="(ra, index) in raList" :key="index">
                        <td>{{ index + 1 }}</td>
                        <td>{{ ra.nama }}</td>
                        <td><a :href="ra.aksi" download class="btn">Download</a></td>
                    </tr>
                </tbody>
            </table>
        </div>
    </section>
</template>

<script setup>
const raList = [
    {nama:"Rencana Aksi Tahun 2023", aksi: "a"},
    {nama:"Rencana Aksi Tahun 2021", aksi: "a"},
    {nama:"Rencana Aksi Tahun 2020", aksi: "a"},
]
</script>

<style scoped>
.ra {
    width: 100%;
    max-width: 2000px;
    background-color: #f4f6f7;
    align-items: center;
    padding: 20px 0;
}

.ra_c{
    padding: 20px;
    background: white;
    border-radius: 8px;
    margin: 0 200px;
    box-shadow: 0 2px 6px rgba(0, 0, 0, 0.1);
    overflow-x: auto;
}

.ra_c h2 {
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
    .ra_c {
        margin: 10px
    }
}

</style>
