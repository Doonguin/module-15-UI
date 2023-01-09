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
            ACCOUNT
        </a>
        <a href="#">
            <img alt="account" src="/public/add.png" />
            ADD TO-DO
        </a>
        <a href="#">
            <img alt="account" src="/public/remove.png" />
            REMOVE TO-DO
        </a>
    </nav>
</template>