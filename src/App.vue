<script setup>
    import Sidebar from './components/Sidebar.vue'
    import List from './components/List.vue'
</script>

<template>
    <header>
        <h1>TO-DO LIST UI WITH VUEJS</h1>
    </header>

    <div id="todo">
        <List titleText="TO-DO LIST" />
    </div>

    <Sidebar />
</template>