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
            Galeri▾
        </a>

        <transition name="expand">
        <div v-if="isOpen" class="mega_m" :class="{ mobile: isMobile }">
          <div class="mega_ti">
            <h1>Galeri</h1>
            <p>Galeri Biro Pengadaan Barang dan Jasa</p>
          </div>
            <div class="mega_c">
              <NuxtLink class="mega_d" to="/galeri2" @click="closeMega">
                <div class="container">
                  <img src="@/assets/info.svg" class="svg-icon" />
                  <div>
                    <a>Pelayanan</a>
                    <p>Galeri Pelayanan pada Biro PBJ</p>
                  </div>
                </div>
              </NuxtLink>
              <NuxtLink class="mega_d" to="/galeri" @click="closeMega">
                <div class="container">
                  <img src="@/assets/image.svg"/>
                  <div>
                    <a>Foto dan Video</a>
                    <p>Galeri Foto dan Video pada Biro PBJ</p>
                  </div>
                </div>
              </NuxtLink>
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
  width: 350px;
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

  .container a {
    color: white;
  }

  .container p {
    display: none;
  }
}

</style>