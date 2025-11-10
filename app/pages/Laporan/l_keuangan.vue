<template>
    <section class="lk">
        <div class="lk_c">
            <h2>Laporan Keuangan</h2>
            <h3> Tahun 2025 </h3>
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
                    <tr v-for="(lk, index) in lkList1" :key="index">
                        <td>{{ index + 1 }}</td>
                        <td>{{ lk.nama }}</td>
                        <td>{{ lk.ukuran }}</td>
                        <td>{{ lk.jumlah }}</td>
                        <td><a :href="lk.aksi" download class="btn">Download</a></td>
                    </tr>
                </tbody>
            </table><br></br>
            <h3> Tahun 2024 </h3>
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
                    <tr v-for="(lk, index) in lkList2" :key="index">
                        <td>{{ index + 1 }}</td>
                        <td>{{ lk.nama }}</td>
                        <td>{{ lk.ukuran }}</td>
                        <td>{{ lk.jumlah }}</td>
                        <td><a :href="lk.aksi" download class="btn">Download</a></td>
                    </tr>
                </tbody>
            </table><br></br>
            <h3> Tahun 2023 </h3>
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
                    <tr v-for="(lk, index) in lkList3" :key="index">
                        <td>{{ index + 1 }}</td>
                        <td>{{ lk.nama }}</td>
                        <td>{{ lk.ukuran }}</td>
                        <td>{{ lk.jumlah }}</td>
                        <td><a :href="lk.aksi" download class="btn">Download</a></td>
                    </tr>
                </tbody>
            </table><br></br>
            <h3> Tahun 2022 </h3>
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
                    <tr v-for="(lk, index) in lkList4" :key="index">
                        <td>{{ index + 1 }}</td>
                        <td>{{ lk.nama }}</td>
                        <td>{{ lk.ukuran }}</td>
                        <td>{{ lk.jumlah }}</td>
                        <td><a :href="lk.aksi" download class="btn">Download</a></td>
                    </tr>
                </tbody>
            </table><br></br>
        </div>
    </section>
</template>

<script setup>
const lkList1 = [
    {nama:"Realisasi / Penyerapan Anggaran (triwulan I) Tahun 2025", ukuran: "5.09 MB", jumlah: "1", aksi: "a"},
]
const lkList2 = [
    {nama:"Capaian Program Kegiatan TW. II Tahun 2024", ukuran: "171.85 KB", jumlah: "1", aksi: "a"},
    {nama:"LRA Tahun 2024", ukuran: "462.28 KB", jumlah: "1", aksi: "a"},
    {nama:"Catatan Atas Laporan Keuangan Tahun 2024", ukuran: "2.58 MB", jumlah: "1", aksi: "a"},
    {nama:"Neraca Tahun 2024", ukuran: "369.31 KB", jumlah: "1", aksi: "a"}
]
const lkList3 = [
    {nama:"1. Laporan Realisasi Anggaran Tahun 2023", ukuran: "2.25 MB", jumlah: "1", aksi: "a"},
    {nama:"2. Catatan Atas Laporan Keuangan Tahun 2023", ukuran: "5.27 MB", jumlah: "1", aksi: "a"},
    {nama:"3. Neraca Tahun 2023", ukuran: "2.12 MB", jumlah: "1", aksi: "a"},
    {nama:"Capaian Realisasi dan Program Kegiatan Tahun 2023", ukuran: "173.38 KB", jumlah: "1", aksi: "a"}
]
const lkList4 = [
    {nama:"1. Laporan Realisasi Anggaran", ukuran: "6.49 MB", jumlah: "1", aksi: "a"},
    {nama:"2. Catatan Atas Laporan Keuangan", ukuran: "24.45 MB", jumlah: "1", aksi: "a"},
    {nama:"3. Daftar Aset Badan Publik", ukuran: "26.15 MB", jumlah: "1", aksi: "a"},
    {nama:"4. Neraca", ukuran: "5.56 MB", jumlah: "1", aksi: "a"}
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

.lk_c{
    padding: 20px;
    background: white;
    border-radius: 8px;
    padding: 1.5rem;
    margin-bottom: 2rem;
    box-shadow: 0 2px 6px rgba(0, 0, 0, 0.1);
    margin-left: 200px;
    max-width: 1000px;
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
