<script setup lang="ts">
import { ref } from 'vue'

const file = ref<File>()
const fileInput = ref<HTMLInputElement>()
const url = ref('')

function fileChange(event: Event) {
  console.log(url.value= URL.createObjectURL(fileInput.value?.files![0]));
}
</script>

<template>
  <input type="file" ref="fileInput" @change="fileChange" name="" id="" />
  <video :src="url"></video>
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
