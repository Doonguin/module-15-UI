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
        <!-- Fill with js because I am funny man -->
    </ul>
</template>

<script defer>

export default {
    mounted() {
        const list = document.getElementsByTagName('ul')[0];

        for (let i = 1; i <= localStorage.getItem('TODO_LENGTH'); i++) {
            list.innerHTML += `<li>ITEM ${i} <input type="checkbox"></li>`;
        }
    }
}

</script>