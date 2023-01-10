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
    <input type="text" name="item" maxlength="100">
    <button>Add item</button>
</template>

<script defer>

export default {
    mounted() {
        const addItem = document.getElementsByTagName('button')[0];
        const itemName = document.getElementsByTagName('input')[0];

        addItem.addEventListener('click', () => {
            for (let i = 0; i <= localStorage.length; i++) {
                if (!localStorage.getItem(`TODO_ITEM_${i}`)) {
                    localStorage.setItem(`TODO_ITEM_${i}`, itemName.value);
                    break;
                } else if (!localStorage.getItem(`TODO_ITEM_${i + 1}`)) {
                    localStorage.setItem(`TODO_ITEM_${i + 1}`, itemName.value);
                    break;
                }
            }

            location.reload();
        });
    }
}

</script>