<template>
    <section class="s1">
        <div class="s2">
            <div class="s3">
                <h2> Struktur Organisasi</h2>
                <img src="@/assets/struktur.jpg" alt="Struktur Organisasi">
            </div>
        </div>
    </section>
</template>

<style scoped>
.s1 {
    padding: 80px 20px;
    background-color: #ffffff;
}

.s2 {
    max-width: 1000px;
    margin: 0 auto;
}

.s3 h2 {
    border-bottom: 2px solid #f1c40f;
    width: 60%;
    padding-bottom: 1%;
}

.s3 img {
    margin-top: 30px;
    width: 800px;
    height: 900px;
    object-fit: cover;
    transition: all 0.3s ease, box-shadow 0.3s ease;
}

.s3 img:hover {
    transform: translateY(-6px);
}

@media (max-width: 768px) {
    .s2 {
        max-width: 100%;
    }

    .s3 img {
        width: 100%;
        object-fit: cover;
        height: auto;
    }

    .s3 h2 {
        width: 55%;
        font-size: 25px;
        text-align: left;
        padding-bottom: 2%;
    }
}


</style>