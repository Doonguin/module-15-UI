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
        window.addEventListener('load', () => {
            const list = document.getElementsByTagName('ul')[0];

            for (let i = localStorage.length - 1; i >= 0; i--) {
                if (localStorage.getItem(localStorage.key(i)) != null) {
                    if (localStorage.getItem(localStorage.key(i)).search('; true') != -1) {
                        list.innerHTML += `<li>${localStorage.getItem(localStorage.key(i)).replace('; true', '')} <input id="${localStorage.key(i)}" type="checkbox"></li>`;

                        // Ik weet niet waarom maar zonder de timeout werkt het niet en het is raar.....
                        // Maar goed, het werkt nu dus ik blijf er van af :)
                        setTimeout(() => {
                            document.getElementById(localStorage.key(i)).checked = true;
                        }, 1);
                    } else {
                        list.innerHTML += `<li>${localStorage.getItem(localStorage.key(i))} <input id="${localStorage.key(i)}" type="checkbox"></li>`;
                    }
                }
            }

            for (let i = localStorage.length-1; i >= 0; i--) {
                let check = document.getElementById(localStorage.key(i));

                check.addEventListener('click', () => {
                    if (check.checked == true) {
                        localStorage.setItem(localStorage.key(i), `${localStorage.getItem(localStorage.key(i))}; true`);
                    } else {
                        localStorage.setItem(localStorage.key(i), `${localStorage.getItem(localStorage.key(i)).replace('; true', '')}`);
                    }
                });
            }
        });
    }
}

</script>