<template>
  <div class="home">
    <div class="main-text">
      <h1>Selamat Datang di<br />SMKN 4 TASIKMALAYA</h1>
    </div>
  </div>
  <section class="offers">
    <div class="offer-content">
      <div class="row">
        <i class="bi bi-person-fill"></i>
        <h3>60</h3>
        <p>GURU</p>
      </div>
      <div class="row">
        <i class="bi bi-award-fill"></i>
        <h3>5</h3>
        <p>JURUSAN</p>
      </div>
      <div class="row">
        <i class="bi bi-people-fill"></i>
        <h3>1116</h3>
        <p>MURID</p>
      </div>
      <div class="row">
        <i class="bi bi-person-workspace"></i>
        <h3>20</h3>
        <p>ADMINISTRASI</p>
      </div>
    </div>
  </section>
  <section class="about" id="about">
    <div class="about-img">
      <img src="assets/kepsek.png" alt="" />
    </div>
    <div class="about-text">
      <h3>SAMBUTAN KEPALA SEKOLAH</h3>
      <p>Assalamu’alaikum Wr. Wb</p>
            <p class="text-jutify">Segala puji dan syukur kehadirat Allah SWT, semoga kita semua dalam lindungan-Nya. dan atas ijin beliau kami dapat menyajikan website SMK Negeri 4 Tasikmalaya ini.
                Kami berharap dengan adanya web site di SMK Negeri 4 Tasikmalaya ini para pengunjung dapat mengenal lebih jauh tentang sekolah kami sehingga dapat mempererat tali silaturrahmi antara sekolah dengan masyarakat demi kemajuan kita bersama.
                Tiada gading yang tak retak, web site kami ini masih dalam proses pengembangan, masih banyak kekurangan yang harus kami perbaiki. Kritik dan sarannya yang membangun sangat kami harapkan untuk pengembangan ke depan.
                Akhirnya, saya mengucapkan terimakasih yang sebesar- besarnya kepada semua pihak yang tidak dapat disebutkan satu persatu atas segala bantuan dan fasilitasnya yang telah diberikan semoga semua yang kita lakukan bermanfaat bagi masyarakat.
                Wassalamu’alaikum Wr, Wb</p>
            <p><strong>Kepala Sekolah</strong><br>Kurniawan, S.Pd., M.Pd.</p>
    </div>
  </section>
  <section class="product" id="product">
    <div class="main-txt">
      <h3>BERITA TERBARU</h3>
    </div>
    <div class="card-content">
      <div class="row">
          <div v-for="teacher in teachers" :key="teacher.id" class="card" style="width: 18rem;margin-left: 3rem; margin-right: 2rem; margin-top: 2rem;margin-bottom: 2rem;">
            <img :src="teacher.image" :alt="teacher.name" class="card-img-top" alt="...">
            <div class="card-body text-center">
                <h5 class="card-title ">{{ teacher.name }}</h5>
                <a :href="teacher.subject" class="card-link">Selengkapnya</a> 
            </div>
        </div>
      </div>
      </div>
      <div class="d-grid gap-2 col-3 mx-auto mt-5">
        <button @click="loadmore" class="btn btn-primary" type="button">Berita Lainnya</button>
      </div>
  </section>
</template>
<style scoped>
@import url("https://cdn.jsdelivr.net/npm/bootstrap-icons@1.11.3/font/bootstrap-icons.min.css");
.home {
  width: 100%;
  height: 100vh;
  background-image: linear-gradient(rgba(0, 0, 0, 0.1), rgba(0, 0, 0, 0.1)),
    url(assets/bg.webp);
  background-repeat: no-repeat;
  background-size: cover;
  background-position: 50%;
}
.home .main-text {
  text-align: center;
  padding: 150px 10% 10px;
}
.main-text h1 {
  font-size: 60px;
  color: #fff;
  text-shadow: 0px 0px 1px black;
}
.home .main-text p {
  color: white;
  margin-top: 5px;
}
#btn {
  width: 200px;
  height: 36px;
  font-weight: bold;
  background: white;
  color: #388b6f;
  letter-spacing: 1px;
  border: 2px solid #388b6f;
  border-radius: 5px;
  margin-top: 10px;
  transition: 0.5s;
  cursor: pointer;
}
#btn:hover {
  background-color: #388b6f;
  color: white;
}
/* Home Section End */

.profil {
  width: 100%;
  height: 100vh;
  background-repeat: no-repeat;
  background-size: cover;
  background-position: 50%;
}
.profil .main-text {
  text-align: center;
  padding: 10px 10% 10px;
}
.profil .main-text h1 {
  font-size: 60px;
  color: #388b6f;
  text-shadow: 0px 0px 1px black;
}

/* Top Section Card Start */
.offers {
  padding: 10px 8% 20px;
  background: #f3f3f3;
}
.offer-content {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, auto));
  align-items: center;
  gap: 0.9rem;
  margin-top: 30px;
}
.offer-content .row {
  position: relative;
  overflow: hidden;
  border-radius: 10px;
  cursor: pointer;
}
.offer-content .row i {
  font-size: 50px;
  color: #388b6f;
}
.offer-content .row h3 {
  margin-left: 5px;
}
.offer-content .row p {
  margin-left: 5px;
}
@media (max-width: 920px) {
  .offer-content {
    grid-template-columns: 1fr;
  }
}
.about {
  padding: 150px 8% 120px;
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  align-items: center;
  gap: 1.5rem;
}
.about-img img {
  max-width: 530px;
  height: auto;
  width: 100%;
  border-radius: 10px;
  box-shadow: rgba(99, 99, 99, 0.2) 0px 2px 8px 0px;
}
.about-text h3 {
  color: #388b6f;
  font-size: 30px;
  line-height: 1;
}
.about-text p {
  color: black;
  letter-spacing: 1px;
  margin-bottom: 4rem;
  margin-top: 10px;
}
#about-btn {
  width: 150px;
  height: 35px;
  background: white;
  border: 2px solid #388b6f;
  color: #388b6f;
  font-weight: bold;
  border-radius: 5px;
  transition: 0.5s;
  cursor: pointer;
}
#about-btn:hover {
  background: #388b6f;
  color: white;
}
@media (max-width: 920px) {
  .about {
    grid-template-columns: 1fr;
  }
  .about-img {
    text-align: center;
    order: 2;
  }
  .about-img img {
    width: 100%;
    height: auto;
    max-width: 100%;
  }
}
/* About Section End */

/* Product Section Start */
.product {
  padding: 10px 8% 120px;
}
.main-txt {
  text-align: center;
}
.main-txt h3 {
  font-size: 36px;
  text-transform: uppercase;
  font-weight: 600;
  color: #388b6f;
  text-shadow: 0px 1px 1px black;
}
.card-content {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, auto));
  align-items: center;
  gap: 0.9rem;
  margin-top: 30px;
}
.card-content .row {
  background: #f3f3f3;
  position: relative;
  overflow: hidden;
  border-radius: 10px;
  cursor: pointer;
}
.row img {
  width: 100%;
  display: block;
}
.card-body {
  padding: 10px;
}
.card-body h3 {
  margin-top: 10px;
  font-size: 30px;
  font-weight: 550;
  color: #388b6f;
  text-shadow: 0px 1px 1px black;
}
.card-body p {
  font-weight: 500;
  margin-top: 5px;
  letter-spacing: 1px;
}
.card-body h5 {
  margin-top: 5px;
  font-size: 18px;
}
.card-body button {
  width: 150px;
  height: 30px;
  font-weight: 550;
  margin-top: 5px;
  background: transparent;
  color: #388b6f;
  border-radius: 5px;
  border: 2px solid #388b6f;
  transition: 0.5s;
  cursor: pointer;
}
.card-body button:hover {
  background: #388b6f;
  color: white;
}
@media (max-width: 920px) {
  .card-content {
    grid-template-columns: 1fr;
  }
}
</style>
<script setup>


// Data guru dengan properti `image`
const db_teachers = ref([
  {
    id: 1,
    name: 'Honda Resmikan Safety Riding Lab di SMKN 4 Tasikmalaya',
    subject:'https://www.pikiran-rakyat.com/otomotif/pr-018109177/honda-resmikan-safety-riding-lab-di-smkn-4-tasikmalaya-ciptakan-bibit-keselamatan-di-jawa-barat?page=all',
    image: new URL('@/assets/news1.jpeg', import.meta.url).href  },
  {
    id: 2,
    name: 'Aplikasi SIMORING, Solusi Kekinian dari Universitas BSI untuk PKL di SMKN 4 Tasikmalaya',
    subject: 'https://news.bsi.ac.id/2024/07/31/aplikasi-simoring-solusi-kekinian-dari-universitas-bsi-untuk-pkl-di-smkn-4-tasikmalaya/',
    image: new URL('@/assets/news2.jpeg', import.meta.url).href  },  
  {
    id: 3,
    name: 'Cegah Geng Motor, SMKN di Tasikmalaya Luncurkan Ekstrakurikuler Unik',
    subject: 'https://bandung.kompas.com/read/2024/07/24/115239678/cegah-geng-motor-smkn-di-tasikmalaya-luncurkan-ekstrakurikuler-unik',
    image: new URL('@/assets/news3.jpg', import.meta.url).href  },  
  {
    id: 4,
    name: 'Polsek Cibeureum Sosialisasikan Larangan Knalpot Brong dan Geng Motor di SMKN 4 Kota Tasikmalaya',
    subject: 'https://tasikmalaya.inews.id/read/502735/polsek-cibeureum-sosialisasikan-larangan-knalpot-brong-dan-geng-motor-di-smkn-4-kota-tasikmalaya',
    image: new URL('@/assets/news4.jpg', import.meta.url).href  }, 
  {
    id: 5,
    name: 'Honda Edukasi Jurnalis di Tasikmalaya, dari Simulator Hingga Prediksi Bahaya di Jalan',
    subject: 'https://radartasik.id/2024/07/24/honda-edukasi-jurnalis-di-tasikmalaya-dari-simulator-hingga-prediksi-bahaya-di-jalan/',
    image: new URL('@/assets/news5.webp', import.meta.url).href  }, 
  {
    id: 6,
    name: 'Siswa SMKN 4 Tasikmalaya Adu Inovasi dan Kreativitas di Expo Creanova',
    subject: 'https://radartasik.id/2023/03/02/siswa-smkn-4-tasikmalaya-adu-inovasi-dan-kreativitas-di-expo-creanova/',
    image: new URL('@/assets/news6.webp', import.meta.url).href  }, 
]);

// Ambil 5 data awal
const teachers = ref([...db_teachers.value.slice(0, 4)]);
const limitStart = ref(teachers.value.length); // Batas awal pengambilan data
const limitEnd = ref(limitStart.value + 4); // Batas akhir pengambilan data

// Fungsi memuat data baru dari db_teachers
const loadmore = () => {
  teachers.value = [...teachers.value, ...db_teachers.value.slice(limitStart.value, limitEnd.value)];
  limitStart.value = limitEnd.value;
  limitEnd.value += 4;
};
</script>
