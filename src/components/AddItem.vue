<script setup>
defineProps({
    qOne: {
        type: String,
        required: true
    }
})
</script>

<template>
    <label for="item">{{ qOne }}</label>
    <input type="text" name="item">
    <button>Add item</button>
</template>