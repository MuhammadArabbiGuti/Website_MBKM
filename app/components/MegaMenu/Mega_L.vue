<template>
    <div class="mega" @mouseleave="closeMega">
        <a @mouseover="openMega" class="mega_b">
            Laporan ▾
        </a>
        <div v-if="isOpen" class="mega_m" >
          <div class="mega_ti">
            <h1>Laporan</h1>
            <p>Dokumen - dokumen berisi Laporan pada Biro Pengadaan Barang dan Jasa</p>
          </div>
          <div class="mega_g">
            <div class="mega_c">
              <NuxtLink class="mega_d" to="/Laporan/pengaduan" @click="closeMega">
                <div class="container">
                  <img src="@/assets/alert-circle.svg"/>
                  <div>
                    <a>Pengaduan</a>
                    <p>Laporan Pengaduan Biro PBJ per bulan</p>
                  </div>
                </div>
              </NuxtLink>
              <NuxtLink class="mega_d" to="/Laporan/l_kinerja" @click="closeMega">
                <div class="container">
                  <img src="@/assets/archive.svg"/>
                  <div>
                    <a>Kinerja</a>
                    <p>Laporan Kinerja Biro PBJ</p>
                  </div>
                </div>
              </NuxtLink>
              <NuxtLink class="mega_d" to="/Laporan/r_pengadaan" @click="closeMega">
                <div class="container">
                  <img src="@/assets/package.svg"/>
                  <div>
                    <a>Realisasi Pengadaan</a>
                    <p>Laporan Realisasi Pengadaan Biro PBJ</p>
                  </div>
                </div>
              </NuxtLink>
            </div>
            <div class="mega_c">
              <NuxtLink class="mega_d" to="/Laporan/lm_resiko" @click="closeMega">
                <div class="container">
                  <img src="@/assets/alert-triangle.svg"/>
                  <div>
                    <a>Manajemen Resiko</a>
                    <p>Laporan Manejemen Resiko Biro PBJ per tahun</p>
                  </div>
                </div>
              </NuxtLink>
              <NuxtLink class="mega_d" to="/Laporan/l_keuangan" @click="closeMega">
                <div class="container">
                  <img src="@/assets/dollar-sign.svg"/>
                  <div>
                    <a>Keuangan</a>
                    <p>Laporan Keuangan Biro PBJ per tahun</p>
                  </div>
                </div>
              </NuxtLink>
              <NuxtLink class="mega_d" to="/Laporan/lm_evaluasi" @click="closeMega">
                <div class="container">
                  <img src="@/assets/monitor.svg"/>
                  <div>
                    <a>Monitoring dan Evaluasi</a>
                    <p>Laporan Monitoring dan Evaluasi Biro PBJ per tahun</p>
                  </div>
                </div>
              </NuxtLink>
            </div>
            <div class="mega_c">
              <NuxtLink class="mega_d" to="/Laporan/skm" @click="closeMega">
                <div class="container">
                  <img src="@/assets/smile.svg"/>
                  <div>
                    <a>SKM</a>
                    <p>Laporan Survey Kepuasan Masyarakat</p>
                  </div>
                </div>
              </NuxtLink>
              <NuxtLink class="mega_d" to="https://forms.gle/6A4HsC2wyxEU2soh7" target="_blank">
                <div class="container">
                  <img src="@/assets/external-link.svg"/>
                  <div>
                    <a>SKM Eksternal</a>
                    <p>Google Form SKM Eksternal</p>
                  </div>
                </div>
              </NuxtLink>
              <NuxtLink class="mega_d" to="https://forms.gle/aDZUDsdosQcsBL5m7" target="_blank">
                <div class="container">
                  <img src="@/assets/external-link.svg"/>
                  <div>
                    <a>SKM Internal</a>
                    <p>Google Form SKM Internal</p>
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
  font-size: 15px;
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
  width: 1200px;
  height: 400px;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0,0,0,0.2);
  justify-content: center;
  z-index: 999;
  top: 105%;  
  left: -300px; 
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
  font-size: 15px;
  display: block;
  color: #333;
  text-decoration: none;
  text-align: center;
  margin-bottom: 0.8rem;
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