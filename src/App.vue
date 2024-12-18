<script setup lang="ts">
import HelloWorld from './components/HelloWorld.vue';
import { ref, reactive } from 'vue';

const message = ref('Hello World!');
const titleClass = ref('title');
const counter = reactive({
  count: 1,
});

counter.count++;
</script>

<template>
  <h1 :class="titleClass">{{ message }}</h1>
  <p>{{ counter.count }}</p>
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
.title {
  color: red;
}
</style>
