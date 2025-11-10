<template>
    <div class="card">
      <h3 class="card-title">{{ title }}</h3>
      <p class="card-desc">{{ description }}</p>
    </div>
</template>
  
<script setup>
  defineProps({
    title: String,
    description: String
  })
</script>
  
<style scoped>

.card {
  background: #fff;
  border-radius: 10px;
  padding: 20px;
  box-shadow: 0px 2px 6px rgba(0, 0, 0, 0.1);
  transition: transform 0.2s;
}
  
.card:hover {
  transform: translateY(-3px);
  background: #d1d1d1
}
  
.card-title {
  font-size:20px;
  font-weight: bold;
  color: #2f6d3f;
  margin-bottom: 10px;
  text-align: center;
}
  
.card-desc {
  font-size: 14px;
  color: #4b5563;
}

</style>
  