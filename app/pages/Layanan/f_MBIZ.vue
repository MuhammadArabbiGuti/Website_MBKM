<template>
    <div class="form-container">
      <h2>Formulir MBIZ Market</h2>
  
      <form @submit.prevent="handleSubmit">
  
        <div class="form-group">
          <label for="email">Email <span class="required">*</span></label>
          <input
            type="email"
            id="email"
            v-model="form.email"
            placeholder="contoh@email.com"
            required
          />
        </div>

        <div class="form-group">
          <label for="pelaku">Pelaku Usaha <span class="required">*</span></label>
          <select id="pelaku" v-model="form.pelaku" required>
          <option value="orang">Orang Perseorangan</option>
          <option value="badan">Badan Usaha</option>
        </select>
        </div>

        <div class="form-group">
          <label for="o_nama">Nama Perusahaan / Institusi / Toko <span class="required">*</span></label>
          <input
            type="text"
            id="o_nama"
            v-model="form.o_nama"
            placeholder="Mohon masukkan nama Perusahaan / Institusi / Toko"
            required
          />
        </div>
  
        <div class="form-group">
          <label for="pesan">Alamat Perusahaan / Institusi / Toko <span class="required">*</span></label>
          <textarea
            id="pesan"
            v-model="form.pesan"
            placeholder="Mohon masukkan Alamat Perusahaan / Institusi / Toko"
            required
          ></textarea>
        </div>

        <div class="form-group">
          <label for="nama">Nama Lengkap <span class="required">*</span></label>
          <input
            type="text"
            id="nama"
            v-model="form.nama"
            placeholder="Mohon masukkan nama lengkap Anda."
            required
          />
        </div>
  
        <button type="submit">Kirim</button>
      </form>
  
      <p v-if="submitted" class="success-msg">
        Formulir berhasil dikirim!
      </p>
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue'
  
  const form = ref({
    email: '',
    pelaku: '',
    o_nama: '',
    pesan: '',
    nama: '',
  })
  
  const submitted = ref(false)
  
  const handleSubmit = () => {
    console.log("Data dikirim:", form.value)
  
    submitted.value = true
    form.value = { email: '', pelaku: '', o_nama: '', pesan: '', nama: '',  }
  }
  </script>
  
<style scoped>

.form-container {
  max-width: 600px;
  margin: 2rem auto;
  background: #fff;
  padding: 2rem;
  border-radius: 8px;
  box-shadow: 0 2px 6px rgba(0,0,0,0.1);
}
  
h2 {
  margin-bottom: 1rem;
  text-align: center;
  color: #064e3b;
}
  
.form-group {
  margin-bottom: 1rem;
}
  
label {
  display: block;
  font-weight: bold;
  margin-bottom: 0.3rem;
}
  
input, textarea {
  width: 100%;
  padding: 0.8rem;
  border: 1px solid #ccc;
  border-radius: 6px;
  font-size: 1rem;
}
  
button {
  display: block;
  width: 100%;
  padding: 0.8rem;
  background: #064e3b;
  color: white;
  font-size: 1rem;
  border: none;
  border-radius: 6px;
  cursor: pointer;
}
  
button:hover {
  background: #046135;
}
  
.success-msg {
  margin-top: 1rem;
  color: green;
  font-weight: bold;
  text-align: center;
}

.required {
  color: red;
  font-weight: bold;
}

</style>
  