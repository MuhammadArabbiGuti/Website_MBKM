<template>
    <div class="page">
        <section class="content">
            <div class="container">
                <h2>Regulasi</h2>
                <div class="grid">
                    <NuxtLink to="https://jdih.lkpp.go.id/" class="card" target="_blank">
                        <h3>Regulasi Pusat</h3>
                    </NuxtLink>
                    <NuxtLink to="https://jdih.kalbarprov.go.id/" class="card" target="_blank">
                        <h3>JDIH</h3>
                    </NuxtLink>
                    <NuxtLink to="/" class="card" target="_blank">
                        <h3>Instruksi Presiden</h3>
                    </NuxtLink>
                    <NuxtLink to="/Regulasi/r_daerah" class="card" target="_blank">
                        <h3>Regulasi Daerah</h3>
                    </NuxtLink>
                    <NuxtLink to="/Regulasi/lkpp" class="card" target="_blank">
                        <h3>LKPP</h3>
                    </NuxtLink>
                    <NuxtLink to="/" class="card" target="_blank">
                        <h3>PUPR</h3>
                    </NuxtLink>
                </div>
            </div>
        </section>
    </div>
</template>

<style scoped>

.content {
  background-color: #f8f9fa;
  padding: 3rem 1rem;
}

.container {
  background: white;
  border-radius: 10px;
  padding: 2rem;
  max-width: 1000px;
  margin: 0 auto;
  box-shadow: 0 2px 6px rgba(0, 0, 0, 0.1);
}

.container h2 {
  margin-bottom: 2rem;
  text-align: center;
}

.grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 1.5rem;
}

.card {
  background: #fff;
  border: 1px solid #e5e5e5;
  border-radius: 8px;
  padding: 1.5rem;
  transition: box-shadow 0.2s;
}
  
.card:hover {
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
}
  
.card h3 {
  margin-bottom: 0.8rem;
  color: #2f6d3f;;
  text-align: center;
}
  
.card p, li {
  color: #333;
  font-size: 0.95rem;
  line-height: 1.5;
}

.card ul {
  list-style-type: none;
  text-align: center;
}

.card li {
  font-size: 18px;
  margin-top: 20px;
}

</style>