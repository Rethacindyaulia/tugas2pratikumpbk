<template>
  <div>
    <!-- Isi komponen HelloWorld di sini -->
    <input
      v-model="text"
      placeholder="Silahkan Diisi..."
      :style="{
        'font-weight': text.length > 7 ? 'bold' : 'normal',
        color: text.length > 7 ? 'red' : 'black',
      }"
    />
    <p v-if="text.length > 0">Yang Anda Buat: {{ text }}</p>
  </div>
</template>

<script setup>
import { ref, defineExpose } from "vue";

// Mendefinisikan variabel reaktif text
const text = ref("");

// Mengekspos variabel text untuk akses dari luar komponen
defineExpose({ text });
</script>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>
