<script>
export default {
    data() {
        return {
            i: 0,
            code: ['ArrowUp', 'ArrowUp', 'ArrowDown', 'ArrowDown', 
                   'ArrowLeft', 'ArrowRight', 'ArrowLeft', 'ArrowRight',
                   'b', 'a', 'Enter']
        }
    },
    computed: {
        text() {
            if(this.i === this.code.length) {
                this.i = 0;
                return 'Konami Code Entered!';
            }   
            return 'Check the console 👀';
        }
    },  
    mounted() {
        console.log('%c ⬆️ ⬆️ ⬇️ ⬇️ ⬅️ ➡️ ⬅️ ➡️ B A ENTER', 'font-size: 1.5rem');

        window.addEventListener('keyup', event => {
            const { key } = event;
            
            if(key === this.code[this.i]) {
                this.i++;
            } else {
                this.i = 0;
            }
        });
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