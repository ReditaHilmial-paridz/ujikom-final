<template>
      <div class="profil">
        <div class="main-text">
            <h1>visi & misi<br>SMKN 4 TASIKMALAYA</h1>
        </div>
        <section class="visimisi" id="about">
            <div class="visi-text">
                <h3>visi</h3>
                <p>TERWUJUDNYA LULUSAN YANG CERDAS, AKTIF, KOMPETITIF, ADAPTIF, DAN PRODUKTIF BERLANDASKAN IMAN DAN TAKWA</p>
    
            </div>
            <div class="misi-text">
                <h3>misi</h3>
                <p>1.Menyiapkan Sumber Daya Manusia yang cerdas dan kompeten baik hardskill maupun softskill. <br>
2.Meningkatkan dan mengembangkan aktifitas serta kreatifitas seluruh warga sekolah dalam berbagai kegiatan positif. <br>
3.Mewujudkan manajemen pengelolaan yang efektif, efesien, transparan, akuntabel dan layanan prima. <br>
4.Menumbuhkan dan mengembangkan potensi dan kemampuan Sumber Daya Manusia yang berdaya saing tinggi melalui berbagai kegiatan akademik maupun non akademik. <br>
5.Menyelenggarakan berbagai program kegiatan dalam upaya meningkatkan Sumber Daya Manusia yang mampu menyesuaikan dengan perkembangan. <br>
6.Mengembangkan sarana prasarana dan lingkungan sekolah yang menyenangkan sebagai wadah menumbuhkembangkan daya kreasi dan inovasi untuk menghasilkan produk teknologi tepat guna. <br>
7.Membangun jiwa wirausaha yang handal melalui pembelajaran Teaching Factory (TEFA) dan Kelas Industri. <br>
8.Menjalin dan mengembangkan kemitraan dengan Industri dan Dunia Kerja (IDUKA) serta lembaga lainnya yang relevan. <br>
9.Menanamkan dan membudayakan sikap dan perilaku yang baik pada aktivitas di sekolah maupun dalam kehidupan sehari-hari. <br>
</p> 
            </div>   
        </section>
    </div>
</template>
<style scoped>
.profil{
    width: 100%;
    height: 100vh;
    background-repeat: no-repeat;
    background-size: cover;
    background-position: 50%;
}
.profil .main-text{
    text-align: center;
    padding: 10px 10% 10px;
}
.profil .main-text h1{
    font-size: 60px;
    color: #388b6f;
    text-shadow: 0px 0px 1px black;
}
  .visimisi{
    padding: 30px 8% 120px;
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    align-items: center;
    gap: 1.5rem;
}
.visi-text h3{
    color: #388b6f;
    font-size: 30px;
    line-height: 1;
}
.misi-text h3{
    color: #388b6f;
    font-size: 30px;
    line-height: 1;
}
.visi-text p{
    color: black;
    letter-spacing: 1px;
    margin-bottom: 4rem;
    margin-top: 10px;
}
.misi-text p{
    color: black;
    letter-spacing: 1px;
    margin-bottom: 4rem;
    margin-top: 10px;
}

</style>