<template>
    <section class="sosmed">
        <div class="social">
            <h2>Social Media:</h2>
                <div class="container">
                    <img src="@/assets/facebook.svg" />
                    <a href="https://www.facebook.com/biropbjkalbar/" target="_blank">Facebook</a>
                </div>
                <div class="container">
                    <img src="@/assets/instagram.svg" />
                    <a href="https://www.instagram.com/barjaskalbar/" target="_blank">Instagram</a>
                </div>
                <div class="container">
                    <img src="@/assets/twitter.svg" />
                    <a href="https://twitter.com/biropbjkalbar" target="_blank">Twitter</a>
                </div>
                <div class="container">
                    <img src="@/assets/youtube.svg" />
                    <a href="https://youtube.com/@biropengadaanbarangdanjasa8573?si=iF_5MyMfOjNc1vxq" target="_blank">Youtube</a>
                </div>
        </div>
    </section>
</template>

<style scoped>

.sosmed{
    background-color: #ffffff;
    max-width: 1000px;
    margin: 0 auto;
    display: flex;
    flex-wrap: wrap;
    align-items: left;
    gap: 40px;
    display: grid;
    grid-template-columns: 1fr 1fr;
    text-align: left;
}

.social{
    padding: 60px 20px;
}

.social img {
    margin-right: 10px;
}

.container {
    display: flex;
    align-items: center;
    gap: 10px;
    margin-bottom: 15px;
    width: 300px;
    height: 60px;
    margin-left: 10px;
}

.container a {
  transition: color 0.3s ease;
  text-decoration: none;
  color: #2f6d3f;;
}

.container a:hover {
  color: #f1c40f; 
}

</style>