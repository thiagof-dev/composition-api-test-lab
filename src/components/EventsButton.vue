<template>
    <button @click="emitEvent">Click to emit an event</button>
</template>

<script setup>
const emit = defineEmits(['buttonClicked'])

const emitEvent = () => {
    emit('buttonClicked')
}




</script>
