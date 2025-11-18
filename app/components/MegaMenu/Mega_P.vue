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
            Pelayanan▾
        </a>
        
        <transition name="expand">
        <div v-if="isOpen" class="mega_m" :class="{ mobile: isMobile }">
          <div class="mega_ti">
            <h1>Pelayanan</h1>
            <p>Dokumen dan Formulir layanan Biro Pengadaan Barang dan Jasa</p>
          </div>

          <div class="mega_g">
            <div class="mega_c1">
                <h3> Dokumen: </h3>
                <NuxtLink class="mega_d" to="/Layanan/standar_p" @click="closeMega">
                <div class="container">
                  <img src="@/assets/bookmark.svg"/>
                  <div class="text">
                    <a>Standar Layanan</a>
                    <p>Dokumen berisi Standar Layanan Biro PBJ</p>
                  </div>
                </div>
                </NuxtLink>
            </div>

            <div class="mega_c">
                <h3>Formulir: </h3>
                <NuxtLink class="mega_d" to="/Layanan/f_pengaduan" @click="closeMega">
                <div class="container">
                  <img src="@/assets/flag.svg"/>
                  <div class="text">
                    <a>Pengaduan</a>
                    <p>Formulir Pengaduan</p>
                  </div>
                </div>
                </NuxtLink>
                <NuxtLink class="mega_d" to="/Layanan/f_pertanyaan" @click="closeMega">
                <div class="container">
                  <img src="@/assets/help-circle.svg"/>
                  <div class="text">
                    <a>Pertanyaan</a>
                    <p>Formulir Pertanyaan</p>
                  </div>
                </div>
                </NuxtLink>
                <NuxtLink class="mega_d" to="/Layanan/f_saranusulan" @click="closeMega">
                <div class="container">
                  <img src="@/assets/message-square.svg"/>
                  <div class="text">
                    <a>Saran dan Usulan</a>
                    <p>Formulir Saran dan Usulan</p>
                  </div>
                </div>
                </NuxtLink>
            </div>

            <div class="mega_c">
                <h3 style="color: white;" :class="{ mobile: isMobile }"> . </h3>
                <NuxtLink class="mega_d" to="/Layanan/f_permintaan" @click="closeMega">
                <div class="container">
                  <img src="@/assets/plus.svg"/>
                  <div class="text">
                    <a>Permintaan</a>
                    <p>Formulir Permintaan Layanan</p>
                  </div>
                </div>
                </NuxtLink>
                <NuxtLink class="mega_d" to="/Layanan/f_surat" @click="closeMega">
                <div class="container">
                  <img src="@/assets/mail.svg"/>
                  <div class="text">
                    <a>Surat</a>
                    <p>Formulir Menyampaikan Surat</p>
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
  width: 1400px;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0,0,0,0.2);
  z-index: 999;
  top: 105%;  
  left: -180%; 
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
  font-size: 20px;
  display: block;
  color: #333;
  text-decoration: none;
  text-align: center;
  margin-bottom: 2rem;
  padding-bottom: 0.3rem;
}

.mega_c p, .mega_c1 p{
  font-size: 15px;
  color: #333;
  font-weight: normal;
  margin: 0;
}

.mega_c a, .mega_c1 a{
  font-size: 18px;
  display: block;
  color: #333;
  text-decoration: none;
  padding: 0.3rem 0;
}

.mega_c1{
  padding-right: 20px; 
  margin-right: 20px; 
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
  gap: 10px;
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