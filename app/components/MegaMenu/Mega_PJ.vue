<script setup>
  import { ref, onMounted, onBeforeUnmount } from 'vue'

  const isOpen = ref(false)
  const isMobile = ref(false)
  
  const openMega = () => {
    if(isMobile.value){
      (isOpen.value = !isOpen.value)
    } else {
      isOpen.value = true
    }
  }
  
  const closeMega = () => {
    if (!isMobile.value) isOpen.value = false
  }

  const checkScreen = () => {
    isMobile.value = window.innerWidth <= 768
  }

  onMounted(() => {
    checkScreen()
    window.addEventListener('resize', checkScreen)
  })
  onBeforeUnmount(() => {
    window.removeEventListener('resize', checkScreen)
  })

</script>

<template>
    <div class="mega" @mouseleave="closeMega" @mouseenter="!isMobile && (isOpen = true)">
        <a @click="openMega" class="mega_b">
            Program Kerja▾
        </a>

        <transition name="expand">
        <div v-if="isOpen" class="mega_m" :class="{ mobile: isMobile }">
          <div class="mega_ti">
            <h1>Program Kerja</h1>
            <p>Dokumen - dokumen berisi Program Kerja pada Biro Pengadaan Barang dan Jasa</p>
          </div>

          <div class="mega_g">
            <div class="mega_c1" >
              <h3> SOP: </h3>
              <NuxtLink class="mega_d" to="/SOP/s_pbj" @click="closeMega">
                <div class="container">
                  <img src="@/assets/home.svg"/>
                  <div class="text">
                    <a>PBJ</a>
                    <p>SOP Bagian Pengelolaan Pengadaan Barang dan Jasa</p>
                  </div>
                </div>
              </NuxtLink>
              <NuxtLink class="mega_d" to="/SOP/s_lpse" @click="closeMega">
                <div class="container">
                  <img src="@/assets/hard-drive.svg"/>
                  <div class="text">
                    <a>LPSE</a>
                    <p>SOP Bagian Pengelolaan LPSE</p>
                  </div>
                </div>
              </NuxtLink>
              <NuxtLink class="mega_d" to="/SOP/s_pa" @click="closeMega">
                <div class="container">
                  <img src="@/assets/clipboard.svg"/>
                  <div class="text">
                    <a>Pembinaan dan Advokasi</a>
                    <p>SOP Bagian Pengelolaan Pembinaan dan Advokasi</p>
                  </div>
                </div>
              </NuxtLink>
            </div>

            <div class="mega_c">
              <h3> Dokumen Lainnya: </h3>
              <NuxtLink class="mega_d" to="/DokumenPK/rencanaumum" @click="closeMega">
                <div class="container">
                  <img src="@/assets/grid.svg"/>
                  <div class="text">
                    <a>RUP</a>
                    <p>Dokumen Rencana Umum Pengadaan biro PBJ</p>
                  </div>
                </div>
              </NuxtLink>
              <NuxtLink class="mega_d" to="/DokumenPK/rencanaaksi" @click="closeMega">
                <div class="container">
                  <img src="@/assets/layout.svg"/>
                  <div class="text">
                    <a>Rencana Aksi</a>
                    <p>Dokumen Rencana Aksi biro PBJ</p>
                  </div>
                </div>
              </NuxtLink>
              <NuxtLink class="mega_d" to="/DokumenPK/renstra" @click="closeMega">
                <div class="container">
                  <img src="@/assets/list.svg"/>
                  <div class="text">
                    <a>Renstra</a>
                    <p>Dokumen Rencana Strategis biro PBJ</p>
                  </div>
                </div>
              </NuxtLink>
              <NuxtLink class="mega_d" to="/DokumenPK/renja" @click="closeMega">
                <div class="container">
                  <img src="@/assets/tool.svg"/>
                  <div class="text">
                    <a>Renja</a>
                    <p>Dokumen Rencana Kerja biro PBJ</p>
                  </div>
                </div>
              </NuxtLink>
            </div>

            <div class="mega_c">
              <h3 style="color: white;" :class="{ mobile: isMobile }"> . </h3> 
              <NuxtLink class="mega_d" to="/DokumenPK/rka" @click="closeMega">
                <div class="container">
                  <img src="@/assets/dollar-sign.svg"/>
                  <div class="text">
                    <a>RKA</a>
                    <p>Dokumen Rencana Kerja dan Anggaran biro PBJ</p>
                  </div>
                </div>
              </NuxtLink>
              <NuxtLink class="mega_d" to="/DokumenPK/cascading" @click="closeMega">
                <div class="container">
                  <img src="@/assets/git-branch.svg"/>
                  <div class="text">
                    <a>Cascading</a>
                    <p>Dokumen Cascading (Penjabaran) biro PBJ</p>
                  </div>
                </div>
              </NuxtLink>
              <NuxtLink class="mega_d" to="/DokumenPK/indikator" @click="closeMega">
                <div class="container">
                  <img src="@/assets/play.svg"/>
                  <div class="text">
                    <a>Indikator Kerja Utama</a>
                    <p>Dokumen Indikator Kerja Utama biro PBJ</p>
                  </div>
                </div>
              </NuxtLink>
              <NuxtLink class="mega_d" to="/DokumenPK/perjanjian" @click="closeMega">
                <div class="container">
                  <img src="@/assets/share-2.svg"/>
                  <div class="text">
                    <a>Perjanjian Kerja</a>
                    <p>Dokumen Perjanjian Kerja biro PBJ</p>
                  </div>
                </div>
              </NuxtLink>
            </div>

            <div class="mega_c">
              <h3 style="color: white;" :class="{ mobile: isMobile }"> . </h3>
              <NuxtLink class="mega_d" to="/DokumenPK/programkegiatan" @click="closeMega">
                <div class="container">
                  <img src="@/assets/activity.svg"/>
                  <div class="text">
                    <a>Program Kegiatan</a>
                    <p>Dokumen Program Kegiatan biro PBJ</p>
                  </div>
                </div>
              </NuxtLink>
              <NuxtLink class="mega_d" to="/DokumenPK/pohonkinerja" @click="closeMega">
                <div class="container">
                  <img src="@/assets/bar-chart.svg"/>
                  <div class="text">
                    <a>Pohon Kinerja</a>
                    <p>Dokumen Pohon Kinerja biro PBJ</p>
                  </div>
                </div>
              </NuxtLink>
            </div>
          </div>
        </div>
      </transition>
    </div>
</template>

<style scoped>

.expand-enter-active, .expand-leave-active {
  transition: all 0.3s ease;
  overflow: hidden;
}

.expand-enter-from, .expand-leave-to {
  max-height: 0;
  opacity: 0;
  transform: translateY(-10px);
}

.expand-enter-to, .expand-leave-from {
  max-height: 800px;
  opacity: 1;
  transform: translateY(0);
}

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
  position: absolute;
  background: #fff;
  padding: 20px;
  width: 1200px;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0,0,0,0.2);
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

.mega_c, .mega_c1 {
  flex: 1;
  margin: 0 1rem;
}

.mega_c h3, .mega_c1 h3 {
  font-size: 17px;
  display: block;
  color: #333;
  text-decoration: none;
  text-align: center;
  margin-bottom: 2rem;
  padding-bottom: 0.3rem;
}

.mega_c p, .mega_c1 p{
  font-size: 11px;
  color: #333;
  font-weight: normal;
  margin: 0;
}

.mega_c a, .mega_c1 a{
  font-size: 14px;
  display: block;
  color: #333;
  text-decoration: none;
  padding: 0.3rem 0;
}

.mega_c1{
  padding-right: 15px; 
  margin-right: 15px; 
  border-right: 1px solid #ddd;
}
  
.mega_d {
  display: block;
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
  gap: 1px;
}

.container div{
  margin-left: 10px;
}

@media (max-width: 768px) {
  .mega_m.mobile {
    position: static;
    background: #2f6d3f;
    color: white;
    box-shadow: none;
    width: 100%;
    padding: 10px 15px;
    transform: translateX(-10%);
  }

  .mega_ti {
    display: none;
  }

  .mega_g {
    flex-direction: column;
  }

  .mega_d {
    background-image: none;
  }

  .mega_d img {
    background-color: #fff;
    border-radius: 100%;
    padding: 2%;
  }

  .mega_d:hover a{
    color: #f1c40f;
    font-weight: 500;
    border-bottom: #fff solid 3px;
  }

  .container a {
    color: white;
  }

  .container p {
    display: none;
  }

  .mega_c1 {
    border: none;
    padding: none;
  }

  .mega_c h3, .mega_c1 h3 {
    color:#f1c40f;
    text-align: left;
  }

  h3.mobile {
    display: none;
  }
}

</style>