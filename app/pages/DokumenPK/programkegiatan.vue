<template>
    <section class="pk">
        <div class="pk_container">
            <h2>Dokumen Program dan Kegiatan</h2>
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
                    <tr v-for="(pk, index) in pkList" :key="index">
                        <td>{{ index + 1 }}</td>
                        <td>{{ pk.nama }}</td>
                        <td>{{ pk.ukuran }}</td>
                        <td>{{ pk.jumlah }}</td>
                        <td><a :href="pk.aksi" download class="btn">Download</a></td>
                    </tr>
                </tbody>
            </table>
        </div>
    </section>
</template>

<script setup>
const  pkList = [
    {nama: "DPA TAHUN 2025", ukuran: "10.19 MB", jumlah: "1", aksi: "Download"},
    {nama: "DPPA 2024 & Angkas Perubahan 2024", ukuran: "12.62 MB", jumlah: "1", aksi: "Download"},
    {nama: "DPA Tahun 2024", ukuran: "66.68 KB", jumlah: "1", aksi: "Download"},
    {nama: "DPA BPBJ 2023", ukuran: "49.90 KB", jumlah: "1", aksi: "Download"},
    {nama: "Program Kegiatan TH. 2023", ukuran: "174.47 KB", jumlah: "1", aksi: "Download"},
    {nama: "RKA 2023", ukuran: "385.42 KB", jumlah: "1", aksi: "Download"}
]
</script>

<style scoped>
.pk {
    padding: 50px 20px;
    padding-left: 0px;
    padding-right: 100px;
    background-color: #f4f6f7;
    align-items: center;
}

.pk_container{
    padding: 20px;
    background: white;
    border-radius: 8px;
    padding: 1.5rem;
    margin-bottom: 2rem;
    box-shadow: 0 2px 6px rgba(0, 0, 0, 0.1);
    margin-left: 200px;
    max-width: 1000px;
}

.btn {
  padding: 5px;
  transition: background-color 0.3s ease;
  border-radius: 10px;
}

.btn:hover {
  text-decoration: none;
  background-color: #f1c40f;
  color: #fff;
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

</style>