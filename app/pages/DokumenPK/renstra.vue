<template>
    <section class="rs">
        <div class="rs_c">
            <h2>Dokumen Renstra (Rencana Strategis)</h2>
            <table>
                <thead>
                    <tr>
                        <th>No</th>
                        <th>Dokumen</th>
                        <th>Aksi</th>
                    </tr>
                </thead>
                <tbody>
                    <tr v-for="(rs, index) in rsList" :key="index">
                        <td>{{ index + 1 }}</td>
                        <td>{{ rs.nama }}</td>
                        <td><a :href="rs.aksi" download class="btn">Download</a></td>
                    </tr>
                </tbody>
            </table>
        </div>
    </section>
</template>

<script setup>
const rsList = [
    {nama:"RENSTRA-Perubahan-BIRO-PBJ", aksi: "a"},
    {nama:"Rencana Strategis Tahun 2019 s/d 2023", aksi: "a"},
    {nama:"RENSTRA-2021", aksi: "a"},
    {nama:"RENSTRA-2020", aksi: "a"}
]
</script>

<style scoped>
.rs {
    padding: 50px 20px;
    padding-left: 200px;
    padding-right: 400px;
    max-width: 1000px;
    background-color: #f4f6f7;
    align-items: center;
}

.rs_c{
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
