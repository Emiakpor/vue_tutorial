<script setup lang="ts">
import { ref, reactive } from 'vue';
const text = ref('');
const text1 = ref('');

function onInput(e){
  text.value = e.target.value
}

</script>

<template>
  <input :value="text" @input="onInput" placeholder="type here"/>
  <p> {{ text }} </p>


  <input v-model="text1" placeholder="type here"/>
  <p> {{ text1 }} </p>
</template>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>