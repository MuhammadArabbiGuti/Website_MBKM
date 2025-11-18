<template>
    <section class="s">
        <div class="s_c">
            <h2>SOP Bagian Pengelolaan LPSE</h2>
            <table>
                <thead>
                    <tr>
                        <th>No</th>
                        <th>Nama</th>
                        <th>Ukuran File</th>
                        <th>Jumlah File</th>
                        <th>Tanggal Pembuatan</th>
                        <th>Pembaruan Terakhir</th>
                        <th>Aksi</th>
                    </tr>
                </thead>
                <tbody>
                    <tr v-for="(SOP, index) in SOPList" :key="index">
                        <td>{{ index + 1 }}</td>
                        <td>{{ SOP.nama }}</td>
                        <td>{{ SOP.ukuran }}</td>
                        <td>{{ SOP.jumlah }}</td>
                        <td>{{ SOP.pembuatan }}</td>
                        <td>{{ SOP.pembaruan }}</td>
                        <td><a :href="SOP.aksi" download class="btn">Download</a></td>
                    </tr>
                </tbody>
            </table>
        </div>
    </section>
</template>

<script setup>
const  SOPList = [
{nama: "SOP Pengembangan Aplikasi", ukuran: "955.46 KBB", jumlah: "1", pembuatan:"12 Juli 2021", pembaruan:"24 Juli 2024", aksi: "Download"},
{nama: "SOP Pengelolaan Tamu", ukuran: "1.56 MB", jumlah: "1", pembuatan:"12 Juli 2021", pembaruan:"12 Juli 2021", aksi: "Download"},
{nama: "SOP Pengaduan", ukuran: "1.41 MB", jumlah: "1", pembuatan:"12 Juli 2021", pembaruan:"12 Juli 2021", aksi: "Download"},
{nama: "SOP Pendaftaran Akun Penyedia", ukuran: "1.49 MB", jumlah: "1", pembuatan:"12 Juli 2021", pembaruan:"12 Juli 2021", aksi: "Download"},
{nama: "SOP Pendaftaran Akun Pengelola Pengadaan Barang dan Jasa", ukuran: "1.38 MB", jumlah: "1", pembuatan:"12 Juli 2021", pembaruan:"12 Juli 2021", aksi: "Download"},
]
</script>

<style scoped>
.s {
    width: 100%;
    max-width: 2000px;
    background-color: #f4f6f7;
    align-items: center;
    padding: 20px 0;
}

.s_c{
    padding: 20px;
    background: white;
    border-radius: 8px;
    margin: 0 200px;
    box-shadow: 0 2px 6px rgba(0, 0, 0, 0.1);
    overflow-x: auto;
}

.s_c h2 {
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
    .s_c {
        margin: 10px
    }
}

</style>