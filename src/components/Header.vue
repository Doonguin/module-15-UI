<script setup>
defineProps({
    page_title: {
        type: String,
        required: true
    }
})
</script>

<template>
    <header>
        <h1>{{ page_title }}</h1>
    </header>
</template>