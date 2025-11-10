<template>
    <section class="lme">
        <div class="lme_container">
            <h2>Laporan Monitoring dan Evaluasi</h2>
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
                    <tr v-for="(lme, index) in lmeList" :key="index">
                        <td>{{ index + 1 }}</td>
                        <td>{{ lme.nama }}</td>
                        <td>{{ lme.ukuran }}</td>
                        <td>{{ lme.jumlah }}</td>
                        <td><a :href="lme.aksi" download class="btn">Download</a></td>
                    </tr>
                </tbody>
            </table>
        </div>
    </section>
</template>

<script setup>
const  lmeList = [
    {nama: "Laporan Monev TW IV 2024", ukuran: "333.91 KB", jumlah: "1", aksi: "Download"},
    {nama: "Laporan Monev TW III 2024", ukuran: "328.97 KB", jumlah: "1", aksi: "Download"},
    {nama: "Laporan Monev TW II 2024", ukuran: "329.04 KB", jumlah: "1", aksi: "Download"},
    {nama: "Laporan Monev TW I 2024", ukuran: "380.74 KB", jumlah: "1", aksi: "Download"},
    {nama: "Laporan Monev TW IV 2023", ukuran: "368.33 KB", jumlah: "1", aksi: "Download"},
    {nama: "Laporan Monev TW III 2023", ukuran: "371.96 KB", jumlah: "1", aksi: "Download"},
    {nama: "Laporan Monev TW II 2023", ukuran: "371.71 KB", jumlah: "1", aksi: "Download"},
    {nama: "Laporan Monev TW I 2023", ukuran: "367.48 KB", jumlah: "1", aksi: "Download"}
]
</script>

<style scoped>

.lme {
    padding: 50px 20px;
    padding-left: 0px;
    padding-right: 100px;
    background-color: #f4f6f7;
    align-items: center;
}

.lme_container{
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