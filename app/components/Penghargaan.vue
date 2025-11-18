<template>
    <section class="p1">
        <div class="p2">
            <div class="p3">
                <h2>Penghargaan</h2>
                <img src="@/assets/penghargaan.jpeg" alt="Penghargaan">
            </div>
        </div>
    </section>
</template>

<style scoped>

.p1 {
    padding: 80px 20px;
    background-color: #fff
}

.p2 {
    max-width: 1000px;
    margin: 0 auto;
}

.p3 h2 {
    border-bottom: 2px solid #f1c40f;
    width: 60%;
    padding-bottom: 1%;
}

.p3 img {
    margin-top: 30px;
    width: 820px;
    height: 600px;
    object-fit: cover;
    border: 2px solid #1b4332;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
    transition: all 0.3s ease, box-shadow 0.3s ease;
}

.p3 img:hover {
    transform: translateY(-6px);
    box-shadow: 0 6px 14px rgba(0, 0, 0, 0.12);
}

@media (max-width: 768px) {
    .p3 img {
        width: 100%;
        object-fit: contain;
        height: auto;
    }

    .p3 h2 {
        width: 55%;
        font-size: 25px;
        text-align: left;
        padding-bottom: 2%;
    }
}

</style>