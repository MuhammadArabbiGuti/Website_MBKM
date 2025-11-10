<template>
    <section class="skm">
        <div class="skm_container">
            <h2>Survey Kepuasan Masyarakat</h2>
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
                    <tr v-for="(skm, index) in skmList" :key="index">
                        <td>{{ index + 1 }}</td>
                        <td>{{ skm.nama }}</td>
                        <td>{{ skm.ukuran }}</td>
                        <td>{{ skm.jumlah }}</td>
                        <td><a :href="skm.aksi" download class="btn">Download</a></td>
                    </tr>
                </tbody>
            </table>
        </div>
    </section>
</template>

<script setup>
const  skmList = [
    {nama: "Laporan Nilai SKM Tahun 2020", ukuran: "857.18 KB", jumlah: "1", aksi: "Download"},
    {nama: "Laporan SKM Tahun 2020", ukuran: "692.05 KB", jumlah: "1", aksi: "Download"},
    {nama: "Laporan SKM 2021", ukuran: "1.70 MB", jumlah: "1", aksi: "Download"}
]
</script>

<style scoped>
.skm {
    padding: 50px 20px;
    padding-left: 0px;
    padding-right: 100px;
    background-color: #f4f6f7;
    align-items: center;
}

.skm_container{
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