<template>
    <section class="j1">
        <div class="j2">
            <div class="j3">
                <h2> Peta Jabatan</h2>
                <img src="" alt="Peta Jabatan">
            </div>
        </div>
    </section>
</template>

<style scoped>
.j1 {
    padding: 80px 20px;
    background-color: #f4f6f7;
}

.j2 {
    max-width: 1000px;
    margin: 0 auto;
}

.j3 h2 {
    border-bottom: 2px solid #f1c40f;
    width: 60%;
    padding-bottom: 1%;
}

.j3 img {
    margin-top: 30px;
    width: 800px;
    height: 900px;
    object-fit: cover;
    border-radius: 100px;
    border: 2px solid #1b4332;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
    transition: all 0.3s ease, box-shadow 0.3s ease;
}

.j3 img:hover {
    transform: translateY(-6px);
    box-shadow: 0 6px 14px rgba(0, 0, 0, 0.12);
}

@media (max-width: 768px) {
    .j3 img {
        width: 100%;
        object-fit: contain;
        height: auto;
    }

    .j3 h2 {
        width: 55%;
        font-size: 25px;
        text-align: left;
        padding-bottom: 2%;
    }
}

</style>