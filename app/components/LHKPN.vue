<template>
    <section class="l">
        <div class="l_container">
            <h2>LHKPN</h2>
            <table>
                <thead>
                    <tr>
                        <th>No</th>
                        <th>Data</th>
                        <th>Aksi</th>
                    </tr>
                </thead>
                <tbody>
                    <tr v-for="(lhkpn, index) in lhkpnList" :key="index">
                        <td>{{ index + 1 }}</td>
                        <td>{{ lhkpn.nama }}</td>
                        <td><a :href="lhkpn.aksi" download class="btn">Lihat</a></td>
                    </tr>
                </tbody>
            </table>
        </div>
    </section>
</template>

<script setup>
const  lhkpnList = [
    {nama: "LHKPN TAHUN 2024 – REKAP", aksi: "tes"},
    {nama: "LHKPN TAHUN 2024 – PEJABAT STRUKTURAL", aksi: "tes"},
    {nama: "LHKPN TAHUN 2024 – KARO", aksi: "tes"},
    {nama: "REKAP LHKPN TAHUN 2023", aksi: "tes"},
    {nama: "LHKPN TAHUN 2023", aksi: "tes"},
    {nama: "WAJIB LHKPN TAHUN 2022", aksi: "tes"},
    {nama: "LHKPN TAHUN 2022 – KARO", aksi: "tes"},
    {nama: "LHKPN TAHUN 2022 – ESELON III DAN IV", aksi: "tes"},
    {nama: "LHKPN TAHUN 2022 – JAFUNG PBJ", aksi: "tes"},
    {nama: "LHKPN TAHUN 2020", aksi: "tes"},
    {nama: "LHKPN TAHUN 2018", aksi: "tes"}
]
</script>

<style scoped>
.l {
    width: 1300px;
    background-color: #f4f6f7;
    align-items: center;
    padding-top: 20px;
    padding-bottom: 20px;
    padding-left: 30px;
    padding-right: 190px;
}

.l_container{
    padding: 20px;
    margin-bottom: 2rem;
    margin-left: 40px;
    margin-top: 20px;
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