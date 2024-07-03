<template>
    <div class="container">
        <img class="about-image" src="@/assets/img/logod.png" alt="Company Logo">
        <hr>
        <h1>Tentang Kami</h1>
        <hr>
        <p>Selamat datang di perusahaan kami. Kami berdedikasi untuk memberikan layanan dan nilai terbaik kepada pelanggan kami. Misi kami adalah memberikan dampak positif di komunitas dan industri kami.</p>
        <hr>
        <h2>Galeri Kue</h2>
        <hr>
        <div class="gallery">
            <div class="gallery-item" v-for="i in 3" :key="i">
                <img src="@/assets/img/8.jpg" :alt="'Kue ' + i">
            </div>
        </div>
        <div class="gallery">
            <div class="gallery-item" v-for="i in 3" :key="i">
                <img src="@/assets/img/12.jpg" :alt="'Kue ' + i">
            </div>
        </div>
        <div class="gallery">
            <div class="gallery-item" v-for="i in 3" :key="i">
                <img src="@/assets/img/9.jpg" :alt="'Kue ' + i">
            </div>
        </div>
        <div class="gallery">
            <div class="gallery-item" v-for="i in 3" :key="i">
                <img src="@/assets/img/10.jpg" :alt="'Kue ' + i">
            </div>
        </div>
        <div class="gallery">
            <div class="gallery-item" v-for="i in 3" :key="i">
                <img src="@/assets/img/3.jpg" :alt="'Kue ' + i">
            </div>
        </div>
        <div class="gallery">
            <div class="gallery-item" v-for="i in 3" :key="i">
                <img src="@/assets/img/11.jpg" :alt="'Kue ' + i">
            </div>
        </div>
        <br>
        <hr>
        <h2>Kontak Kami</h2>
        <hr>
        <br>
        <form @submit.prevent="submitForm" class="contact-form">
            <div class="form-group">
                <label for="name">Nama:</label>
                <input type="text" id="name" v-model="form.name" required>
            </div>
            <div class="form-group">
                <label for="email">Email:</label>
                <input type="email" id="email" v-model="form.email" required>
            </div>
            <div class="form-group">
                <label for="message">Pesan:</label>
                <textarea id="message" v-model="form.message" required></textarea>
            </div>
            <button type="submit" class="btn btn-primary">Kirim</button>
        </form>
        <hr>
        <h2>Alamat Perusahaan</h2>
        <p>Jalanin aja dulu No. 22, Kota Malang, Provinsi Jawa Timur, 2210</p>
        <hr>
        <h2>About Founder</h2>
        <p>Nama Pemilik: Silvi Dwi Anggraini</p>
        <p>Email: camecill@contoh.com</p>
        <p>Telepon: +62 812-3456-7890</p>
    </div>
</template>

<script setup>
import { ref } from 'vue';

const form = ref({
    name: '',
    email: '',
    message: ''
});

const submitForm = () => {
    console.log('Form Submitted:', form.value);
    // Handle form submission logic here (e.g., send data to the server)
};
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

h2 {
    font-size: 2em;
    margin-bottom: 20px;
    color: #444;
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

.gallery {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    justify-content: center;
    margin-top: 20px;
}

.gallery-item {
    flex: 1 1 calc(33% - 20px); /* Three items per row, adjust as needed */
    border-radius: 10px;
    overflow: hidden;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
    transition: transform 0.3s, box-shadow 0.3s;
}

.gallery-item img {
    width: 100%;
    height: auto;
    display: block;
}

.gallery-item:hover {
    transform: scale(1.05);
    box-shadow: 0 6px 15px rgba(0, 0, 0, 0.2);
}

.contact-form {
    max-width: 600px;
    margin: 0 auto;
    text-align: left;
}

.form-group {
    margin-bottom: 20px;
}

label {
    display: block;
    margin-bottom: 5px;
    font-weight: bold;
}

input, textarea {
    width: 100%;
    padding: 10px;
    border: 1px solid #ddd;
    border-radius: 4px;
    font-size: 16px;
}

textarea {
    resize: vertical;
    height: 100px;
}

button {
    padding: 10px 20px;
    font-size: 16px;
    background-color: #a7336d;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    transition: background-color 0.3s;
}

button:hover {
    background-color: #475869;
}
</style>
