<template>
    <nav>
        <a href="#">
            <img alt="account" src="/account.png" />
            ACCOUNT
        </a>
        <a href="#" name="add">
            <img alt="account" src="/add.png" />
            ADD TO-DO
        </a>
        <a href="#">
            <img alt="account" src="/remove.png" />
            REMOVE TO-DO
        </a>
        <a href="#">
            <img alt="about" src="/about.png" />
            ABOUT
        </a>
    </nav>
</template>

<script defer>

export default {
    mounted() {
        const addItem = document.getElementsByName('add')[0];
        const form = document.getElementById('addItemContainer');
        let active = false;

        addItem.addEventListener('click', () => {
            if (!active) {
                form.classList.add('active');
                active = true;
                return;
            }
            
            form.classList.remove('active');
            active = false;
        });
    }
}

</script>