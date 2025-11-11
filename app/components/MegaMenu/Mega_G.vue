<template>
    <div class="mega" @mouseleave="closeMega">
        <a @mouseover="openMega" class="mega_b">
            Galeri ▾
        </a>
        <div v-if="isOpen" class="mega_m" >
          <div class="mega_ti">
            <h1>Galeri</h1>
            <p>Galeri Biro Pengadaan Barang dan Jasa</p>
          </div>
            <div class="mega_c">
              <NuxtLink class="mega_d" to="/galeri2">
                <div class="container">
                  <img src="@/assets/info.svg" class="svg-icon" />
                  <div>
                    <a>Pelayanan</a>
                    <p>Galeri Pelayanan pada Biro PBJ</p>
                  </div>
                </div>
              </NuxtLink>
              <NuxtLink class="mega_d" to="/galeri">
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
  width: 350px;
  height: 285px;
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
  width: 400px;
  height: 60px;
}

.container div{
  margin-left: 10px;
}

</style>