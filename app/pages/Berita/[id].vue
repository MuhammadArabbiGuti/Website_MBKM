<script setup>
import { computed } from "vue"

const route = useRoute()
const id = route.params.id

const { data, pending, error } = await useFetch(
  "https://awdiv2.kalbarprov.go.id/api/site_articles/pbj.kalbarprov.go.id?page=1"
)

const berita = computed(() => {
  return data.value?.data?.data?.find(item => item.id == id)
})

const hasThumbnail = (thumb) => {
  if (!thumb) return false
  return /\.(jpg|jpeg|png|webp)$/i.test(thumb)
}

const getImage = (path) => {
  return "https://" + path
}

const extractFiles = (html) => {
  const regex = /href="([^"]+\.(pdf|docx|xlsx))"/gi
  let result = []
  let match

  while ((match = regex.exec(html)) !== null) {
    result.push(match[1])
  }

  return result
}

const lampiran = computed(() => {
  return extractFiles(berita.value?.content || "")
})

const cleanContent = computed(() => {
  return berita.value?.content
    ?.replace(/<a[^>]*href="[^"]+\.(pdf|docx|xlsx)"[^>]*>.*?<\/a>/gi, "")
})

const getFileName = (url) => {
  return url.split("/").pop()
}
</script>

<template>
  <div class="container">
    
    <div v-if="pending">Loading...</div>
    <div v-else-if="error">Gagal mengambil data</div>
    <div v-else-if="!berita">Berita tidak ditemukan</div>

    <div v-else>
         <NuxtLink to="/berita/berita">← Kembali</NuxtLink>

        <h1>{{ berita.title }}</h1>

        <div class="berita-page">
            <div class="content" v-html="cleanContent"></div>
        </div>

        <div class="lampiran-box" v-if="lampiran.length">
          <ul>
            <li v-for="file in lampiran" :key="file">
              <a :href="file" target="_blank" download>
                <img src="@/assets/pdf.svg" class="pdf"/>
                {{ getFileName(file) }}
                <span class="download">Download</span>
              </a>
            </li>
          </ul>
        </div>

        <img 
            v-if="hasThumbnail(berita.thumbnail)" 
            :src="getImage(berita.thumbnail)" 
            class="thumbnail"
        />
    </div>
  </div>
</template>

<style scoped>
.container {
  max-width: 800px;
  margin: auto;
  padding: 20px;
  display: flex;
  gap: 1rem;
}

.tanggal {
  color: gray;
  margin-bottom: 10px;
}

img {
  width: 100%;
  margin: 15px 0;
  border-radius: 8px;
}

.berita-page .content *{
  color: #333;
}

h1{
  color: #333;
}

.lampiran-box {
  margin: 20px 0;
  padding: 15px;
  border: 1px solid #ddd;
  border-radius: 8px;
  background: #f9f9f9;
}

.lampiran-box h3 {
  margin-bottom: 10px;
}

.lampiran-box ul {
  list-style: none;
  padding: 0;
}

.lampiran-box li {
  margin-bottom: 8px;
}

.lampiran-box a {
  display: flex;
  align-items: center;
  gap: 10px;
  padding: 10px;
  background: #fff;
  border-radius: 6px;
  color: #333;
  border: 1px solid #eee;
}

.lampiran-box a:hover {
  background: #f1f1f1;
}

.icon {
  font-size: 20px;
}

.download {
  margin-left: 6rem;
  color: #0077cc;
  font-size: 1rem;
}

.pdf {
    height: 80px;
    width: 60px;
    margin-left: 20px;
    margin-top: 15px;
}

</style>