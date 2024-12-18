<template>
<button v-on:click="increment">Count is : {{ counter.count }}</button>
</template>

<script setup lang="ts">
import { ref, reactive } from 'vue';

const counter = reactive({
  count: 1,
});

function increment(){
  counter.count++;
}

</script>

<style scoped>

</style>