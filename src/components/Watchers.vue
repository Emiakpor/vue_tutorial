<template>
    <p>{{ message }} </p>

    <button @click="increament">Increament</button>
</template>

<script setup lang="ts">
    import { ref, watch } from 'vue';

    const count = ref(0);
    const message = ref('');

    watch(count, (newCount) => {
        message.value =`New count is: ${newCount}`
    })

    function increament() {
        count.value++;
    }
</script>

<style scoped>

</style>