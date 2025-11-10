<script>
    import Sosmed from './Sosmed.vue';
</script>

<template>
    <section class="contacts">
        <div class="grid">
            <div class="address">
            <ul class="address_list">
                <li><b>Alamat : </b><p>Biro Pengadaan Barang Dan Jasa Sekretariat Daerah Provinsi Kalimantan Barat, 
                    Lantai 3 Gedung Utama (Sayap Barat), Kantor Gubernur Kalimantan Barat, Jl. Jenderal Ahmad Yani, 
                    Bansir Darat, Kecamatan Pontianak Tenggara, Kota Pontianak, Kalimantan Barat, 78124.</p></li>
                <li><b>Email : </b><p>
                    <a href="mailto:helpdesk@lpse.kalbarprov.go.id;">helpdesk@lpse.kalbarprov.go.id;</a>
                    <br>
                    <a href="mailto:pbj@kalbarprov.go.id">pbj@kalbarprov.go.id</a>
                </p></li>
                <li><b>Chat : </b><p>6281513402226</p></li>
                <li><b>Telepon : </b><p>(0561) 736541 Ext. 283</p></li>
                <li><b>Maps : </b><a href="https://maps.app.goo.gl/vacPpydQtDKYPLmY7" target="_blank">https://maps.app.goo.gl/vacPpydQtDKYPLmY7</a></li>
            </ul>
            </div>
            <Sosmed class="sosial"/>
        </div>
    </section>
</template>

<style scoped>

.contacts{
    background-color: #f4f6f7;
}

.grid {
    max-width: 1200px;
    margin: 0 auto;
    display: flex;
    flex-wrap: wrap;
    align-items: right;
    gap: 40px;
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    text-align: left;
}

.grid.sosial{
    align-items: right;
}

.address {
    padding: 60px 20px;
}

.address_list p{
    color:#444;
}

.address_list a {
  transition: color 0.3s ease;
  text-decoration: none;
  color: #2f6d3f;;
}

.address_list a:hover {
  color: #f1c40f; 
}

</style>