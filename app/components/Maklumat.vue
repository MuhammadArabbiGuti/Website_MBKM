<template>
    <section class="m1">
        <div class="m2">
            <div class="m3">
                <h2> Maklumat Pelayanan</h2>
                <img src="@/assets/maklumat.jpeg" alt="Maklumat Pelayanan">
            </div>
        </div>
    </section>
</template>

<style scoped>

.m1 {
    padding: 80px 20px;
    background-color: #ffffff;
}

.m2 {
    max-width: 1000px;
    margin: 0 auto;
}

.m3 h2 {
    border-bottom: 2px solid #f1c40f;
    width: 60%;
    padding-bottom: 1%;
}

.m3 img {
    margin-top: 30px;
    width: 820px;
    height: 600px;
    object-fit: cover;
    border: 2px solid #1b4332;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
    transition: all 0.3s ease, box-shadow 0.3s ease;
}

.m3 img:hover {
    transform: translateY(-6px);
    box-shadow: 0 6px 14px rgba(0, 0, 0, 0.12);
}

@media (max-width: 768px) {
    .m3 img {
        width: 100%;
        object-fit: contain;
        height: auto;
    }

    .m3 h2 {
        width: 55%;
        font-size: 25px;
        text-align: left;
        padding-bottom: 2%;
    }
}

</style>