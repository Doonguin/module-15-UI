<script setup>
defineProps({
    titleText: {
        type: String,
        required: true
    }
})
</script>

<template>
    <h2>{{ titleText }}</h2>

    <ul>
        <li>ITEM 1</li>
        <li>ITEM 2</li>
        <li>ITEM 3</li>
    </ul>
</template>