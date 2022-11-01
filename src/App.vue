<script>
export default {
    data() {
        return {
            text: 'Check the console 👀'
        }
    },
    mounted() {
        console.log('%c ⬆️ ⬆️ ⬇️ ⬇️ ⬅️ ➡️ ⬅️ ➡️ B A ENTER', 'font-size: 1.5rem');
    }
}
</script>

<template>
    <p>{{text}}</p>
</template>

<style scoped>
    p {
        font-size: 5rem;
    }
</style>