<template>
    <div class="container">
        <img class="about-image" src="@/assets/img/logod.png" alt="Company Logo">
        <h1>{{ tulisan }}</h1>
        <h2>Hasil penjumlahan bilangan: {{ hasil }}</h2>

        <div class="form-group">
            <label for="inputAngkaSatu">Angka 1</label>
            <input type="number" id="inputAngkaSatu" v-model="inputAngkaSatu" class="form-control" placeholder="Masukkan angka pertama"/>
        </div>
        <div class="form-group">
            <label for="inputAngkaDua">Angka 2</label>
            <input type="number" id="inputAngkaDua" v-model="inputAngkaDua" class="form-control" placeholder="Masukkan angka kedua"/>
        </div>
        <button @click="proses" class="btn btn-primary btn-block">Hitung Penjumlahan</button>
    </div>
</template>

<script setup>
import { ref } from 'vue'

const tulisan = ref('Kalkulator Sederhana')
const hasil = ref(null)
const inputAngkaSatu = ref('')
const inputAngkaDua = ref('')

const proses = () => {
   const angkaSatu = parseFloat(inputAngkaSatu.value)
   const angkaDua = parseFloat(inputAngkaDua.value)
   if (!isNaN(angkaSatu) && !isNaN(angkaDua)){
       hasil.value = angkaSatu + angkaDua
   } else {
       hasil.value = "Masukkan angka yang valid"
   }
}
</script>

<style scoped>
.container {
    font-family: 'Gill Sans', 'Gill Sans MT', 'Calibri', 'Trebuchet MS', sans-serif;
    max-width: 500px;
    margin: 40px auto;
    padding: 20px;
    text-align: center;
    background-color: #ffffff;
    border-radius: 10px;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
    transition: all 0.3s ease-in-out;
}

.container:hover {
    transform: scale(1.02);
    box-shadow: 0 6px 15px rgba(0, 0, 0, 0.2);
}

.about-image {
    height: 200px; /* Adjust logo size */
    width: 200px; /* Ensure proportional width */
    margin-bottom: 30px; /* Adjust margin for spacing */
}

h1 {
    margin-bottom: 20px;
    font-size: 28px;
    color: #333333;
}

h2 {
    margin-bottom: 20px;
    font-size: 22px;
    color: #666666;
}

.form-group {
    margin-bottom: 15px;
    text-align: left;
}

label {
    font-weight: bold;
    margin-bottom: 5px;
    display: block;
}

input {
    padding: 12px;
    width: calc(100% - 24px);
    border: 1px solid #ddd;
    border-radius: 4px;
    font-size: 16px;
    margin-bottom: 10px;
}

input::placeholder {
    color: #aaa;
}

button {
    padding: 12px 20px;
    font-size: 18px;
    background-color: #a7336d;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    transition: background-color 0.3s;
    width: 100%;
    margin-top: 10px;
}

button:hover {
    background-color: #475869;
}
</style>
