<script setup>
defineProps({
    msg: {
        type: String,
        required: true
    }
})
</script>

<template>
    <nav>
        <a href="#">
            <img alt="account" src="/public/account.png" />
        </a>
        <a href="#">
            <img alt="account" src="/public/add.png" />
        </a>
        <a href="#">
            <img alt="account" src="/public/remove.png" />
        </a>
    </nav>
</template>