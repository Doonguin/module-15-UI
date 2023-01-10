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
        <li>
            ITEM 1
            <input type="checkbox">
        </li>
        <li>
            ITEM 2
            <input type="checkbox">
        </li>
        <li>
            ITEM 3
            <input type="checkbox">
        </li>
    </ul>
</template>