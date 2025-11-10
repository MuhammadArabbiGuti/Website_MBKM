<template>
    <div class="mega" @mouseleave="closeMega">
        <a @mouseover="openMega" class="mega_b">
            Program Kerja ▾
        </a>
        <div v-if="isOpen" class="mega_m" >
          <div class="mega_ti">
            <h1>Program Kerja</h1>
            <p>Dokumen - dokumen berisi Program Kerja pada Biro Pengadaan Barang dan Jasa</p>
          </div>
          <div class="mega_g">
            <div class="mega_c" style="padding-right: 20px; margin-right: 20px; border-right: 1px solid #ddd;">
              <h3> SOP: </h3>
              <NuxtLink class="mega_d" to="/SOP/s_pbj" @click="closeMega">
                <div class="container">
                  <img src="@/assets/logo.png"/>
                  <div class="text">
                    <a>PBJ</a>
                    <p>SOP Bagian Pengelolaan Pengadaan Barang dan Jasa</p>
                  </div>
                </div>
              </NuxtLink>
              <NuxtLink class="mega_d" to="/SOP/s_lpse" @click="closeMega">
                <div class="container">
                  <img src="@/assets/logo.png"/>
                  <div class="text">
                    <a>LPSE</a>
                    <p>SOP Bagian Pengelolaan LPSE</p>
                  </div>
                </div>
              </NuxtLink>
              <NuxtLink class="mega_d" to="/SOP/s_pa" @click="closeMega">
                <div class="container">
                  <img src="@/assets/logo.png"/>
                  <div class="text">
                    <a>Pembinaan dan Advokasi</a>
                    <p>SOP Bagian Pengelolaan Pembinaan dan Advokasi</p>
                  </div>
                </div>
              </NuxtLink>
            </div>
            <div class="mega_c">
              <h3 style="color: white;"> . </h3>
              <NuxtLink class="mega_d" to="/DokumenPK/rencanaumum" @click="closeMega">
                <div class="container">
                  <img src="@/assets/logo.png"/>
                  <div class="text">
                    <a>RUP</a>
                    <p>Dokumen Rencana Umum Pengadaan biro PBJ</p>
                  </div>
                </div>
              </NuxtLink>
              <NuxtLink class="mega_d" to="/DokumenPK/rencanaaksi" @click="closeMega">
                <div class="container">
                  <img src="@/assets/logo.png"/>
                  <div class="text">
                    <a>Rencana Aksi</a>
                    <p>Dokumen Rencana Aksi biro PBJ</p>
                  </div>
                </div>
              </NuxtLink>
              <NuxtLink class="mega_d" to="/DokumenPK/renstra" @click="closeMega">
                <div class="container">
                  <img src="@/assets/logo.png"/>
                  <div class="text">
                    <a>Renstra</a>
                    <p>Dokumen Rencana Strategis biro PBJ</p>
                  </div>
                </div>
              </NuxtLink>
              <NuxtLink class="mega_d" to="/DokumenPK/renja" @click="closeMega">
                <div class="container">
                  <img src="@/assets/logo.png"/>
                  <div class="text">
                    <a>Renja</a>
                    <p>Dokumen Rencana Kerja biro PBJ</p>
                  </div>
                </div>
              </NuxtLink>
            </div>
            <div class="mega_c">
              <h3> Dokumen Lainnya: </h3> 
              <NuxtLink class="mega_d" to="/DokumenPK/rka" @click="closeMega">
                <div class="container">
                  <img src="@/assets/logo.png"/>
                  <div class="text">
                    <a>RKA</a>
                    <p>Dokumen Rencana Kerja dan Anggaran biro PBJ</p>
                  </div>
                </div>
              </NuxtLink>
              <NuxtLink class="mega_d" to="/DokumenPK/cascading" @click="closeMega">
                <div class="container">
                  <img src="@/assets/logo.png"/>
                  <div class="text">
                    <a>Cascading</a>
                    <p>Dokumen Cascading (Penjabaran) biro PBJ</p>
                  </div>
                </div>
              </NuxtLink>
              <NuxtLink class="mega_d" to="/DokumenPK/indikator" @click="closeMega">
                <div class="container">
                  <img src="@/assets/logo.png"/>
                  <div class="text">
                    <a>Indikator Kerja Utama</a>
                    <p>Dokumen Indikator Kerja Utama biro PBJ</p>
                  </div>
                </div>
              </NuxtLink>
              <NuxtLink class="mega_d" to="/DokumenPK/perjanjian" @click="closeMega">
                <div class="container">
                  <img src="@/assets/logo.png"/>
                  <div class="text">
                    <a>Perjanjian Kerja</a>
                    <p>Dokumen Perjanjian Kerja biro PBJ</p>
                  </div>
                </div>
              </NuxtLink>
            </div>
            <div class="mega_c" style="padding-right: 10px;">
              <h3 style="color: white;"> . </h3>
              <NuxtLink class="mega_d" to="/DokumenPK/programkegiatan" @click="closeMega">
                <div class="container">
                  <img src="@/assets/logo.png"/>
                  <div class="text">
                    <a>Program Kegiatan</a>
                    <p>Dokumen Program Kegiatan biro PBJ</p>
                  </div>
                </div>
              </NuxtLink>
              <NuxtLink class="mega_d" to="/DokumenPK/pohonkinerja" @click="closeMega">
                <div class="container">
                  <img src="@/assets/logo.png"/>
                  <div class="text">
                    <a>Pohon Kinerja</a>
                    <p>Dokumen Pohon Kinerja biro PBJ</p>
                  </div>
                </div>
              </NuxtLink>
            </div>
          </div>
        </div>
    </div>
</template>

<script setup>
    import { ref } from 'vue'

    const isOpen = ref(false)
    const openMega = () => (isOpen.value = true)
    const closeMega = () => (isOpen.value = false)
</script>

<style scoped>

.mega{
  position: relative;
}

.mega_b{
  background: none;
  border: none;
  color: white;
  cursor: pointer;
  transition: color 0.3s ease;
}

.mega_b:hover {
  color: #f1c40f; 
  text-decoration: none;
}

.mega_m {
  display: block;
  position: absolute;
  background: #fff;
  padding: 20px;
  width: 1400px;
  height: 600px;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0,0,0,0.2);
  justify-content: center;
  z-index: 999;
  top: 105%;  
  left: 50%; 
  transform: translateX(-50%); 
}

.mega_g {
  display: flex;
  justify-content: space-between;
}

.mega_ti{
  white-space: nowrap;
  display: block;
  text-decoration: none;
  text-align: left;
  border-bottom: 1px solid #ddd;
  margin-bottom: 1.5rem;
  padding-bottom: 1rem;
  text-align: center;
}

.mega_ti h1{
  font-size: 17px;
  color: #2f6d3f;
  margin: 0 0 0.5rem;
}

.mega_ti p{
  font-size: 15px;
  color: #333;
  font-weight: normal;
  margin: 0;
}

.mega_c {
  flex: 1;
  margin: 0 1rem;
}

.mega_c h3 {
  font-size: 20px;
  display: block;
  color: #333;
  text-decoration: none;
  text-align: center;
  margin-bottom: 2rem;
  padding-bottom: 0.3rem;
}

.mega_c p{
  font-size: 15px;
  color: #333;
  font-weight: normal;
  margin: 0;
}

.mega_c a{
  font-size: 18px;
  display: block;
  color: #333;
  text-decoration: none;
  padding: 0.3rem 0;
}
  
.mega_d {
  text-decoration: none;
  margin-bottom: 20px;
  transition: transform 0.3s ease;
  transition: background-size 0.2s linear;
  color: #dfe5f3;
  background-image: linear-gradient(white, white),
  linear-gradient(#f1c40f, #f1c40f);
  background-size: 100% 2px, 0 2px;
  background-position: 100% 100%, 100% 100%;
  background-repeat: no-repeat;
}

.mega_d:hover {
  transform: scale(1.05);
  background-size: 0 0.1em, 100% 0.1em;
}

.mega_d:hover a{
  color: #2f6d3f;
  font-weight: 500;
}

.mega_d img{
  width: 30px;
  max-height: 100px;
}

.container{
  display: flex;
  align-items: center;
  gap: 10px;
  margin-bottom: 15px;
  width: 300px;
  height: 60px;
}

.container div{
  margin-left: 10px;
}

</style>