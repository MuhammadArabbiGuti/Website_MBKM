<template>
    <section class="visimisi">
        <div class="vm_container">
            <div class="visi">
                <h2> Visi </h2>
                <p class="visi_teks">
                    Terwujudnya Kesejahteraan Masyarakat Kalimantan Barat
                    Melalui Percepatan Pembangunan Infrastruktur dan Perbaikan Tata Kelola Pemerintahan
                </p>
            </div>
            <div class="misi">
                <h2> Misi </h2>
                <ol class="misi_teks">
                    <li>Mewujudkan Percepatan Pembangunan Infrastruktur.</li>
                    <li>Mewujudkan Tata Kelola Pemerintahan Berkualitas dengan Prinsip-Prinsip Good Governance.</li>
                    <li>Mewujudkan Masyarakat Yang Sehat, Cerdas, Produktif, dan Inovatif.</li>
                    <li>Mewujudkan Pembangunan Berwawasan Lingkungan.</li>
                </ol>
            </div>
        </div>
    </section>
</template>

<style scoped>

.visimisi {
    background-color: #f4f6f7;
    padding: 60px 20px;
    text-align: center;
}

.visimisi h2 {
    font-size: 40px;
    font-weight: 700;
    color: #1b4332;
    margin-bottom: 16px;
}

.visimisi p {
    font-size: 25px;
    color: #333;
    max-width: 800px;
    margin: 0 auto 40px;
    padding: 0;
    list-style-position: inside
}

.vm_container {
    max-width: 1000px;
    margin: 0 auto;
    display: flex;
    flex-wrap: wrap;
    align-items: left;
    gap: 200px;
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    text-align: center;
}

.visi_teks{
    color:  #444;;
}

.misi ol{
    padding: 0;
    margin: 0 auto 40px;
    max-width: 800px;
    list-style-position: inside
}

.misi ol li{
    font-size: 16px;
    color: #444;
    margin-bottom: 10px;
    text-align: left;
}

</style>