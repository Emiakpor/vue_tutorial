<template>
 <button @click="toggle"> Toggle </button>
 <h1 v-if="awesome">Vue is awesome!</h1>
 <h1 v-else>Oh no!</h1>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const awesome = ref(true);

function toggle() {
    awesome.value = !awesome.value;
}
</script>

<style scoped>

</style>