<template>
  <div class="container">
    <img class="about-image" src="@/assets/img/logod.png" alt="Company Logo">
    <hr>
    <h1>Beranda</h1>
    <hr>
    <p>Selamat datang di situs Kalkulator Online kami!</p>
    <p>
      Situs ini menyediakan berbagai alat kalkulator untuk membantu Anda dalam
      perhitungan sehari-hari, baik itu perhitungan matematis dasar, perhitungan
      keuangan, hingga konversi satuan. Kami berkomitmen untuk memberikan
      pengalaman pengguna yang mudah dan intuitif, sehingga Anda dapat
      menyelesaikan perhitungan dengan cepat dan akurat.
    </p>
    <p>
      Jelajahi berbagai fitur kami dan temukan kalkulator yang sesuai dengan
      kebutuhan Anda. Jika Anda memiliki pertanyaan atau masukan, jangan ragu
      untuk menghubungi kami melalui halaman <router-link to="/about">Tentang</router-link>.
    </p>
  </div>
</template>

<script setup>
</script>

<style scoped>
.container {
    font-family: 'Gill Sans', 'Gill Sans MT', 'Calibri', 'Trebuchet MS', sans-serif;
    max-width: 900px; /* Adjust max-width as needed */
    margin: 40px auto; /* Add margin for spacing */
    padding: 40px;
    text-align: center;
    background-color: #ffffff; /* Change background color for contrast */
    border-radius: 10px;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
    transition: all 0.3s ease-in-out;
}

.container:hover {
    transform: scale(1.02);
    box-shadow: 0 6px 15px rgba(0, 0, 0, 0.2);
}

h1 {
    font-size: 2.5em; /* Increase font size for emphasis */
    margin-bottom: 20px;
    color: #333;
}

p {
    font-size: 1.2em;
    line-height: 1.6;
    margin-bottom: 30px;
    color: #555;
}

.about-image {
    width: 200px; /* Adjust width as needed */
    height: auto;
    border-radius: 8px;
    margin-bottom: 30px; /* Add margin-bottom for separation */
}
</style>
