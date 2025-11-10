<template>
    <div class="card">
      <img src="@/assets/pdf.svg" class="pdf"/>
      <div class="card-contents">
        <h3 class="card-title">{{ title }}</h3>
        <div class="card-detail">
            <img src="@/assets/file-plus.svg" /> 
            <p>Jumlah File: {{ quantity }}</p> 
            <img src="@/assets/database.svg" /> 
            <p>Ukuran: {{ size }}</p>
        </div>
      </div>
      <a href="a" class="button" download><img src="@/assets/download.svg" />Download</a>
    </div>
</template>

<script setup>
    defineProps({
        title: String,
        quantity: Number,
        size: String
    })
</script>

<style scoped>

.card {
    display: flex;
    gap: 30px;
    background: #fff;
    width: 60%;
    height: 120px;
    border-radius: 10px;
    border: 1px #2f6d3f solid;
    box-shadow: 0px 2px 6px rgba(0, 0, 0, 0.1);
    transition: transform 0.2s;
    margin-top: 10px;
    margin-bottom: 10px;
    margin-left: 50px;
}

.card-contents {
    display: flex;
    flex-direction: column;
    text-align: left;
}

.pdf {
    height: 80px;
    width: 60px;
    margin-left: 20px;
    margin-top: 15px;
}
  
.card-title {
    font-size:20px;
    font-weight: bold;
    color: #2f6d3f;
    text-align: left;
}

.card-detail {
    width: 300px;
    display: flex;
    flex-direction: row;
}

.card-detail p {
    padding-right: 20px;
    margin-left: 5px;
}

.card p {
    color: #333;
}

.button {
    margin-left: 35%;
    margin-top: 40px;
    height: 20px;
    background-color: #2f6d3f;
    padding: 10px;
    border-radius: 10px;
    text-decoration: none;
    color: white;
    transition: background-color 0.3s ease;
    display: flex;
    flex-direction: row;
}

.button img {
    margin-right: 15px;
}

.button:hover {
    background-color: #f1c40f;
}

</style>