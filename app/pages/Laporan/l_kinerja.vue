<template>
    <section class="lk">
        <div class="lk_container">
            <h2>Laporan Kinerja</h2>
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
                    <tr v-for="(lk, index) in lkList" :key="index">
                        <td>{{ index + 1 }}</td>
                        <td>{{ lk.nama }}</td>
                        <td>{{ lk.ukuran }}</td>
                        <td>{{ lk.jumlah }}</td>
                        <td><a :href="lk.aksi" download class="btn">Download</a></td>
                    </tr>
                </tbody>
            </table>
        </div>
    </section>
</template>

<script setup>

const  lkList = [
    {nama: "LAPORAN KINERJA 2024", ukuran: "7.03 MB", jumlah: "1", aksi: "Download"},
    {nama: "LAPORAN KINERJA 2023", ukuran: "728.24 KB", jumlah: "1", aksi: "Download"},
    {nama: "LAPORAN KINERJA 2022", ukuran: "1.10 MB", jumlah: "1", aksi: "Download"},
    {nama: "LAPORAN KINERJA 2021", ukuran: "728.24 KB", jumlah: "1", aksi: "Download"},
    {nama: "Laporan Kinerja Tahun 2020", ukuran: "683.23 KB", jumlah: "1", aksi: "Download"},
    {nama: "REKAP PELANGGARAN PENGAWASAN INTERNAL TAHUN 2022", ukuran: "46.65 KB", jumlah: "1", aksi: "Download"},
    {nama: "REKAP PELANGGARAN LAPORAN MASYARAKAT TAHUN 2022", ukuran: "35.79 KB", jumlah: "1", aksi: "Download"},
    {nama: "PROGRAM KEGIATAN DAN CAPAIAN TAHUN 2023", ukuran: "174.47 KB", jumlah: "1", aksi: "Download"},
    {nama: "REKAP PELANGGARAN PENGAWASAN INTERNAL TAHUN 2023", ukuran: "44.40 KB", jumlah: "1", aksi: "Download"},
    {nama: "REKAP PELANGGARAN LAPORAN MASYARAKAT TAHUN 2023", ukuran: "35.34 MB", jumlah: "1", aksi: "Download"}
]
</script>

<style scoped>
.lk {
    padding: 50px 20px;
    padding-left: 0px;
    padding-right: 100px;
    background-color: #f4f6f7;
    align-items: center;
}

.lk_container{
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