<template>
    <section class="s">
        <div class="s_c">
            <h2>SOP Bagian Pembinaan dan Advokasi</h2>
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
{nama: "SOP Permohonan Pemakaian Ruang Rapat", ukuran: "632.30 KB", jumlah: "1", pembuatan:"12 Juli 2021", pembaruan:"12 Juli 2021", aksi: "Download"},
{nama: "SOP Permintaan ATK", ukuran: "673.50 KB", jumlah: "1", pembuatan:"12 Juli 2021", pembaruan:"12 Juli 2021", aksi: "Download"},
{nama: "SOP Penyusunan Renja Biro", ukuran: "739.76 KB", jumlah: "1", pembuatan:"12 Juli 2021", pembaruan:"12 Juli 2021", aksi: "Download"},
{nama: "SOP Penyusunan Penetapan Indikator Kinerja Biro PBJ", ukuran: "991.19 KB", jumlah: "1", pembuatan:"12 Juli 2021", pembaruan:"12 Juli 2021", aksi: "Download"},
{nama: "SOP Penyusunan Laporan Keuangan Biro", ukuran: "607.69 KB", jumlah: "1", pembuatan:"12 Juli 2021", pembaruan:"12 Juli 2021", aksi: "Download"},
]
</script>

<style scoped>
.s {
    padding: 50px 20px;
    padding-left: 200px;
    padding-right: 400px;
    width: 1000px;
    background-color: #f4f6f7;
    align-items: center;
}

.s_c{
    margin-left: 100px;
    padding: 20px;
    background: white;
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