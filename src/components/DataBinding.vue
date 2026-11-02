<script setup>
import { ref } from 'vue';

const count = ref(0);
const bgColor = ref('');
const email = ref('aaa');

const toggleBgColor = () => {
  if(bgColor.value === '') {
    bgColor.value = 'bg-red';
  } else {
    bgColor.value = '';
  }
}
</script>

<template>
  <div @click="count++" class="btn-cnt" :class="bgColor">Count is {{ count }}</div>
  <button @click="count = 0">Count Reset</button>
  <button @click="count--">Count Down</button>
  <button @click="bgColor = 'bg-red'">Red</button>
  <button @click="bgColor = ''">cadetblue</button>
  <button @click="toggleBgColor()">Toggle</button>
  <br><br>
  <input type="text" v-model="email">
  {{ email }}
</template>

<style>
.btn-cnt {
  width: 100px;
  height: 100px;
  background-color: #5f9ea0;
}
.bg-red {
  background-color: #ff0000;
}
</style>