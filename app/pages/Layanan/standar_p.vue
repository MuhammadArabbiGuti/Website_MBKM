<template>
    <section class="sp">
        <div class="sp_container">
            <h2>Dokumen Standar Pelayanan</h2>
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
                    <tr v-for="(sp, index) in spList" :key="index">
                        <td>{{ index + 1 }}</td>
                        <td>{{ sp.nama }}</td>
                        <td>{{ sp.ukuran }}</td>
                        <td>{{ sp.jumlah }}</td>
                        <td><a :href="sp.aksi" download class="btn">Download</a></td>
                    </tr>
                </tbody>
            </table>
        </div>
    </section>
</template>

<script setup>
const  spList = [
    {nama: "SK Tim Pelayanan Publik, Visi, Misi, Moto, Maklumat", ukuran: "5.15 MB", jumlah: "1", aksi: "Download"},
    {nama: "SK Penetapan Standar Pelayanan Publik Pada Biro PBJ", ukuran: "15.54 MB", jumlah: "1", aksi: "Download"},
    {nama: "SK Pengelolaan Pengaduan", ukuran: "4.45 MB", jumlah: "1", aksi: "Download"}
]
</script>

<style scoped>
.sp {
    padding: 50px 20px;
    padding-left: 0px;
    padding-right: 100px;
    background-color: #f4f6f7;
    align-items: center;
}

.sp_container{
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