<template>
    <button @click="send">Greetings</button>
</template>

<script setup lang="ts">
    const emit = defineEmits(['response']);
    
    function send() {
        emit('response', 'hello from child');
    }
</script>

<style scoped>
</style>