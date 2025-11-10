<template>
    <section class="info-cards">
      <div class="card">
        <img src="assets/zona-integritas2.jpg"></img>
      </div>
  
      <div class="card">
        <img src="assets/nilai.jpg"></img>
      </div>
  
      <div class="card">
        <img src="assets/melayani.jpg"></img>
      </div>
    </section>
</template>
  
<style scoped>
  
.info-cards {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 20px;
  padding: 60px 20px;
  max-width: 1200px;
  margin: 0 auto;
}
  
.card {
  background: #ffffff;
  border: 1px solid #e5e5e5;
  border-radius: 8px;
  padding: 30px 20px;
  text-align: center;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.06);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}
  
.card:hover {
  transform: translateY(-6px);
  box-shadow: 0 6px 14px rgba(0, 0, 0, 0.12);
}

.card img {
  max-width: 300px;
  max-height: 400px;
  width: auto;
  height: auto;
  color: #000;
  display: flex;
  align-items: center;
  justify-content: center;
  margin: 0 auto 0 auto;
}

</style>
  