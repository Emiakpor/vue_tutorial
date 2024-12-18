<template>
    <p>{{ message }} </p>

    <button @click="increament">Increament</button>
</template>

<script setup lang="ts">
    import { ref, watch } from 'vue';
    const props = defineProps({
        msg: String
    })

    const count = ref(0);
    const message = ref('');

    watch(count, (newCount) => {
        message.value =`${props.msg}: ${newCount}`
    })

    function increament() {
        count.value++;
    }
</script>

<style scoped>

</style>