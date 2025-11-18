<template>
    <section class="rka">
        <div class="rka_c">
            <h2>Dokumen RKA (Rencana Kerja Anggaran)</h2>
            <table>
                <thead>
                    <tr>
                        <th>No</th>
                        <th>Data</th>
                        <th>Ukuran File</th>
                        <th>Jumlah File</th>
                        <th>Aksi</th>
                    </tr>
                </thead>
                <tbody>
                    <tr v-for="(rka, index) in rkaList" :key="index">
                        <td>{{ index + 1 }}</td>
                        <td>{{ rka.nama }}</td>
                        <td>{{ rka.ukuran }}</td>
                        <td>{{ rka.jumlah }}</td>
                        <td><a :href="rka.aksi" download class="btn">Download</a></td>
                    </tr>
                </tbody>
            </table>
        </div>
    </section>
</template>

<script setup>
const  rkaList = [
    {nama: "RKA 2025", ukuran: "8.28 MB", jumlah: "1", aksi: "Download"},
    {nama: "RKA Perubahan 2024", ukuran: "11.01 MB", jumlah: "1", aksi: "Download"},
    {nama: "RKA 2023", ukuran: "14.27 MB", jumlah: "1", aksi: "Download"},
    {nama: "RKA 2022", ukuran: "385.42 KB", jumlah: "1", aksi: "Download"}
]
</script>

<style scoped>
.rka {
    width: 100%;
    max-width: 2000px;
    background-color: #f4f6f7;
    align-items: center;
    padding: 20px 0;
}

.rka_c {
    padding: 20px;
    background: white;
    border-radius: 8px;
    margin: 0 200px;
    box-shadow: 0 2px 6px rgba(0, 0, 0, 0.1);
    overflow-x: auto;
}

.rka_c h2 {
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
    .rka_c {
        margin: 10px
    }
}

</style>