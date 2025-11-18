<template>
    <footer class="footer">
      <div class="footer_container">
        <div class="footer_about">
          <h3>Biro Pengadaan Barang dan Jasa</h3>
          <p>
            Sekretariat Daerah Provinsi Kalimantan Barat
          </p>
          <img src="@/assets/logo.png" />
        </div>
  
        <div class="footer_contact">
          <h4>Kontak</h4>
          <div class="contact_container">
            <img src="@/assets/map-pin.svg"></img>
            <p>Jl. Jenderal Ahmad Yani, Bansir Darat, Kecamatan Pontianak Tenggara, Kota Pontianak, Kalimantan Barat, 78124.</p>
          </div>
          <div class="contact_container">
            <img src="@/assets/phone-call.svg"></img>
            <p>(0561) 736541 Ext. 283</p>
          </div>
          <div class="contact_container">
            <img src="@/assets/mail2.svg"></img>
            <p>pbj.kalbarprov.go.id</p>
          </div>
        </div>
  
        <div class="footer_links">
          <h4>Tautan Cepat</h4>
          <div>
            <ul class="l1">
              <li><a href="/">Home</a></li>
              <li><a href="/profile">Profil</a></li>
              <li><a href="/programkerja">Program Kerja</a></li>
              <li><a href="/regulasi">Regulasi</a></li>
              <li><a href="/pelayanan">Pelayanan</a></li>
              <li><a href="/laporan">Laporan</a></li>
            </ul>
            <ul class="l2">
              <li><a href="/Berita/berita">Arsip Berita</a></li>
              <li><a href="/galeri">Galeri</a></li>
              <li><a href="/unduhan">Unduhan</a></li>
              <li><a href="https://pbj.kalbarprov.go.id/ppid/">PPID</a></li>
              <li><a href="/kontak">Kontak</a></li>
            </ul>
          </div>
        </div>
      </div>
  
      <div class="footer_bottom">
        <p>© 2025 Biro Pengadaan Barang dan Jasa - Provinsi Kalimantan Barat</p>
      </div>
    </footer>
</template>
  
<style scoped>

.footer {
  background-color: #2f6d3f; 
  color: #ffffff;
  padding: 40px 20px 20px;
}

.footer_container {
  max-width: 1200px;
  margin: 0 auto;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
  gap: 200px;
}

.footer_about{
  text-align: left;
}
  
.footer_about h3 {
  font-size: 20px;
  margin-bottom: 10px;
  font-weight: bold;
  color: #ffffff;
  border-bottom: solid #f1c40f 2px;
  padding-bottom: 5%;
}
  
.footer_about p {
  font-size: 15px;
  line-height: 1.5;
}

.footer_about img {
  height: 130px;
  width: 100px;
  margin-top: 30px;
}
  
.footer_contact h4, .footer_links h4 {
  font-size: 18px;
  margin-bottom: 30px;
  font-weight: bold;
  border-bottom: solid #f1c40f 2px;
  padding-bottom: 5%;
  margin-top: 50px;
}
  
.footer_contact p {
  margin: 6px 0;
  font-size: 15px;
}

.contact_container {
  display: flex;
  align-items: center;
  gap: 10px;
  margin-bottom: 15px;
  width: 300px;
  height: 60px;
  margin-left: 10px;
}
  
.footer_contact img {
  margin-right: 10px;
}

.footer_links h4 {
  text-align: left;
  margin-right: 70px;
}

.footer_links div {
  display: flex;
  flex-direction: row;
  gap: 30px;
}

.footer_links ul {
  list-style: none;
  margin: 0;
  padding: 0;
}
  
.footer_links li {
  margin: 6px 0;
  margin-top: 10px;
}

.footer_links .l1 {
  text-align: left;
}

.footer_links .l2 {
  text-align: right;
}
  
.footer_links a {
  color: #ffffff;
  text-decoration: none;
  transition: color 0.3s ease;
}
  
.footer_links a:hover {
  color: #f1c40f; 
}
  
.footer_bottom {
  margin-top: 30px;
  padding-top: 15px;
  border-top: 1px solid rgba(255, 255, 255, 0.3);
  text-align: center;
}
  
.footer_bottom p {
  font-size: 14px;
  margin: 0;
}

@media (max-width: 768px) {
  .footer_container {
    gap: 20px;
  }

  .footer_about {
    text-align: center;
  }

  .footer_contact {
    text-align: center;
  }

  .footer_contact h4, .footer_links h4, .footer_about h3 {
    border-bottom: none;
    padding-bottom: 0%;
  }

  .footer_about, .footer_contact, .footer_links div {
    border-bottom: solid #f1c40f 2px;
    padding-bottom: 5%;
  }

  .footer_links {
    text-align: center;
    padding: 0;
  }

  .footer_links h4 {
    margin-left: 100px;
  }

  .footer_links div {
    display: flex;
    flex-direction: row;
    gap: 110px;
    text-align: right;
    margin-left: 10px;
  } 
}

</style>
  